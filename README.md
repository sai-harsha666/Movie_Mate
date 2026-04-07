# Movie_Mate
 MovieMate — Conversational AI for Intelligent Movie Search
MovieMate is a complete RAG-powered (Retrieval-Augmented Generation) movie discovery chatbot. It uses 100% open-source and locally runnable components to help users find movies through natural language conversation.

 Architecture & Components
The system is built using the following open-source stack:

Component	Model / Library
Embeddings	sentence-transformers/all-MiniLM-L6-v2
Text Generation	microsoft/Phi-3-mini-4k-instruct
Vector Search	faiss-cpu
Interface	Gradio
Data Source	Local TMDB CSV (TMDB_movie_dataset_v11.csv)
 Installation
To set up the environment, install the following dependencies:

Bash
pip install -q transformers sentence-transformers faiss-cpu gradio \
    accelerate bitsandbytes pandas numpy matplotlib seaborn \
    plotly tqdm scikit-learn huggingface_hub python-dotenv
 Configuration
The project uses the following default configuration parameters:

Dataset Path: TMDB_movie_dataset_v11.csv

Vector Index Storage: embeddings/faiss.index

Retrieval Depth (Top-K): 5 movies

Max New Tokens: 512

 Key Features
Privacy-First: Designed to read the TMDB dataset directly from a local path, requiring no internet connection for data loading once the models are cached.

Efficient Search: Uses FAISS (Facebook AI Similarity Search) for high-speed vector retrieval across a large dataset of movies.

Automated Data Processing: Includes a custom loading pipeline that maps raw TMDB columns (like release_date, vote_average, and poster_path) to a clean format suitable for the chatbot.

Rich Metadata: Each search result includes the title, release year, rating, genre, duration, and overview.

MovieMate — powered by local data and open-source HuggingFace models.
