# Search Engine Project Documentation

## Project Overview
This is a simplified search engine implementation for indexing and searching HTML documents using Python, demonstrating key information retrieval concepts.

## Approach and Algorithms

### Indexing Strategy
The search engine uses two primary data structures for efficient indexing and searching:
1. **Trie (Prefix Tree)**: Used for fast word lookup and storage
2. **Inverted Index**: Maps words to the documents containing them

### Key Components

#### 1. Preprocessing
- HTML parsing using BeautifulSoup
- Text extraction and normalization
- Stop word removal to focus on meaningful terms

#### 2. Indexing Process
- Extract words from each HTML document
- Build a Trie data structure for quick word retrieval
- Create an inverted index mapping words to document indexes

#### 3. Search Mechanism
- Supports multi-word queries
- Uses set intersection to find documents containing all query terms
- Ranks documents based on term frequency

### Data Structures

#### TrieNode
```python
class TrieNode:
    def __init__(self):
        self.children = {}  # Dictionary to store child nodes
        self.is_end_of_word = False  # Indicates complete word
        self.index = None  # Document index reference
```

#### Trie
- Enables efficient prefix-based word searching
- O(k) time complexity for insertion and lookup, where k is word length
- Supports fast prefix matching and retrieval

#### Inverted Index
- Maps each word to a list of document indexes
- Allows quick identification of documents containing specific terms
- Uses Python's `defaultdict` for efficient storage

### Ranking Algorithm
Document ranking is based on:
- Frequency of query terms in the document
- Higher frequency indicates higher relevance
- Simple yet effective ranking approach

## Limitations and Potential Improvements
1. Basic stop word list
2. Simple ranking mechanism
3. No advanced text processing (stemming, lemmatization)
4. Limited to local HTML files

## Requirements
- Python 3.x
- BeautifulSoup4
- Recommended: Virtual environment

## Usage
1. Prepare HTML documents in a directory
2. Update `doc_paths` in the script
3. Run the script
4. Enter space-separated query words

## Example Query
```
Enter query words separated by spaces: machine learning
```

## Future Enhancements
- Advanced text preprocessing
- More sophisticated ranking algorithms
- Support for more document types
- Scalability improvements

## Algorithmic Complexity
- Indexing: O(N * M), where N is number of documents, M is average document length
- Search: O(Q), where Q is the number of query terms
- Ranking: O(R * M), where R is number of result documents

## Conclusion
This search engine demonstrates fundamental information retrieval techniques using Python's data structures and libraries.
