There is a private repository clone too for this public repository.

**Patent Mining of Quantum Computing Innovations**

This project performs NLP-based Patent Mining to analyze the innovation landscape in Quantum Computing since January 1, 2025. Patent data is sourced from Lens.org and focuses on top firms like Google, IBM, Intel, Cisco, Amazon, IonQ, Bull SAS, Classiq, and Fujitsu.

The workflow leverages TF-IDF, Word2Vec, and Topic Modeling (LDA) to uncover research themes, semantic clusters, and innovation trends.

**📌 Features**

Text Preprocessing: Cleans and tokenizes patent titles.

TF-IDF Analysis: Extracts top keywords per document.

Word2Vec Embeddings: Captures semantic similarity of terms, with PCA visualization.

Topic Modeling (LDA): Identifies dominant innovation themes in patents.

Final Output: Enriched dataset with assigned topics → Quantum-Computing_with_topics.csv.

**⚙️ Installation**

Clone this repository and install required dependencies:

git clone https://github.com/yourusername/quantum-patent-mining.git
cd quantum-patent-mining

pip install -r requirements.txt


Or manually install:

pip install gensim pyLDAvis nltk pandas matplotlib scikit-learn

**📂 Dataset**

The project expects an input CSV:

Quantum-Computing.csv → Patent data exported from Lens.org.

Must contain a column: Title (patent titles).

**🚀 Usage**

Run the main script:

python assignment_week6_code.py

Workflow

Preprocessing

Converts text to lowercase

Removes numbers/punctuation

Tokenizes & removes stopwords (including patent-specific stopwords like system, method, thereof)

TF-IDF Analysis

Extracts top 10 keywords per document

Word2Vec Training

Learns embeddings of words in patents

Finds most similar words to quantum and qubit

Reduces embeddings with PCA for 2D visualization

Topic Modeling (LDA)

Extracts 3 major topics from the corpus

Assigns dominant topic + probability to each patent

Final Output

Saves enriched dataset → Quantum-Computing_with_topics.csv

**📊 Example Outputs**

Word2Vec Similarity

Query Word	Similar Words

quantum	computing, circuit, qubits, error, state
qubit	quantum, error, computing, low, circuit

LDA Topics (Interpretation)

Hybrid Quantum-Classical Systems (methods, hybrid, learning)

Hardware Innovations (ion-trap, gates, circuits, devices)

Error Correction & Fault Tolerance (codes, correction, qubits)

**📦 Output Files**

Quantum-Computing_with_topics.csv → Original dataset + dominant topic assignments.

PCA scatter plot of word embeddings.

PyLDAvis interactive visualization (inside Jupyter Notebook).

**🧑‍💻 Tech Stack**

Python 3.9+

NLTK → text preprocessing

scikit-learn → TF-IDF & PCA

Gensim → Word2Vec & LDA

Matplotlib → visualizations

pyLDAvis → topic modeling visualization
