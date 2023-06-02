# Vector Space Model

This program implements a Vector Space Model (VSM) using the Lucene library. The VSM is used for information retrieval and ranking of documents based on their relevance to a given query. The program follows the following steps:

1. Build Zonal Indexes: Two zonal indexes are created, one for the title and another for the abstract of the documents. This allows for efficient searching and retrieval of specific document zones. The tf × idf weighting scheme is used to construct weighted vectors, which helps in assigning importance to terms based on their frequency and rarity.

2. User Interface: The program provides a simple command-line interface to prompt the user for a query or information need. The user can enter a 3-digit integer corresponding to a query/information need from the Cranfield collection (as specified in the cran.qry file). Additionally, the user can specify boost values to indicate relative weights for the title and abstract matches. For example, a boost value pair of (0.7, 0.3) assigns a weight of 0.7 to the title match and 0.3 to the abstract match.

3. Compute Similarity: The program computes the similarity between the user's query and the corpus documents using the cosine similarity score. The cosine similarity measures the angle between two vectors, where a smaller angle indicates a higher similarity.

4. Show Ranked Documents: The program displays the titles of the ranked documents that are relevant to the query. Optionally, it can also show the abstract of the top k matches.

## Usage

1. Install the Lucene library (version 9.0.0) and ensure it is properly configured.

2. Compile the program using the provided source code.

3. Prepare the Cranfield collection and query files:
   - Ensure you have the Cranfield collection of documents.
   - Prepare the cran.qry file containing the queries or information needs corresponding to 3-digit integers.

4. Run the program:
   - Launch the program from the command line or terminal.
   - Follow the prompts to enter a query/information need and specify boost values.
   - The program will compute the similarity using cosine similarity score and display the ranked documents.

5. Evaluate the retrieval performance:
   - Design test cases based on the cranqrel file or any other evaluation criteria.
   - Execute the test cases and document the results.
   - Compare the retrieval performance of the system with the expert-provided answers from cranqrel.

## Dependencies

This program relies on the following dependencies:
- Lucene 9.0.0: The Lucene library is used for indexing, searching, and ranking documents based on the Vector Space Model.

## Contributors

- [Andrew Edwards](https://github.com/andwards)
- [Gabrielle Stein](https://github.com/gabriellestein)
