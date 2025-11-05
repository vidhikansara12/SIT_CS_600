# Search Engine Output Demonstration

## Test Scenario 1: Successful Multi-Document Search
```
Enter search query (or 'quit' to exit): machine learning

Matched Documents: {1, 3, 4}

Ranked Documents by Relevance:
sample_docs/machine_learning.html - Relevance Score: 3
sample_docs/artificial_intelligence.html - Relevance Score: 2
sample_docs/data_science.html - Relevance Score: 1
```

## Test Scenario 2: Single Document Match
```
Enter search query (or 'quit' to exit): python

Matched Documents: {2, 4}

Ranked Documents by Relevance:
sample_docs/programming.html - Relevance Score: 2
sample_docs/data_science.html - Relevance Score: 1
```

## Test Scenario 3: No Document Match
```
Enter search query (or 'quit' to exit): blockchain

No documents found for the query.
```

## Test Scenario 4: Case Insensitivity
```
Enter search query (or 'quit' to exit): ARTIFICIAL intelligence

Matched Documents: {3}

Ranked Documents by Relevance:
sample_docs/artificial_intelligence.html - Relevance Score: 3
```

## Test Scenario 5: Multiple Word Search
```
Enter search query (or 'quit' to exit): machine computer science

Matched Documents: {3, 4}

Ranked Documents by Relevance:
sample_docs/artificial_intelligence.html - Relevance Score: 3
sample_docs/data_science.html - Relevance Score: 2
```

## Final Test: Quit Functionality
```
Enter search query (or 'quit' to exit): quit
Exiting the search engine.
```
