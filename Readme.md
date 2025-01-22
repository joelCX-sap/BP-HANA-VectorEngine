Introduction
In this use case, we will embark on a journey to explore the capabilities of SAP HANA Cloud vector engine, SAP Generative AI Hub and the Langchain Framework. The goal is to equip you with the knowledge and skills to handle unstructured and semi-structured data and build efficient applications.

Embed structured and semi-structured data using Large Language Models (LLMs) from SAP Generative AI Hub. Once the data is embedded, it will be stored in SAP HANA Cloud helping to store and query vector embeddings seamlessly.

Retrieval Augmented Generation in generative AI Hub using SAP HANA vector search
Hands-on Retrieval Augmented Generation (RAG) workflow
The Retrieval Augmented Generation use case process consists of steps to be completed as seen in the graphic below.


title


Documents to be included in vector analysis are fed into the model.

The contents of the files are split into smaller chunks.

Embedding functions are used to create embeddings from the file/document chunks.

The embeddings are then stored as vectors in the SAP HANA Cloud Database.

When a query or prompt is submitted, the query itself is then embedded into vector form.

The query vector is compared to the values stored as vectors in SAP HANA Cloud via a similarity/semantic search.

The most appropriate results are forwarded, along with the original query, to a large language model such as Chat GPT.

The LLM uses the results of the HANA vector search to augment its own searching capabilities, and the final answer is returned to the user.

Setup and configuration
Install required Python modules
Implementing RAG Embeddings
Prepare the documentation for the product catalog in CSV format with each row representing a product.

Connect to the HANA vector storage instance and create a table to store the documentation data.

Populate the table with data and create a REAL_VECTOR column to store embeddings.

Use the Generative AI Hub SDK to define a function to generate embeddings for prompts and perform similarity search using the embeddings.

Enhancing Query Responses
Define a prompt template to provide context to queries.

Modify the function to query the LLM (Large Language Model) based on the prompt template.

Test the model's response using specific queries related to the node library, ensuring it provides contextually relevant responses based on embeddings.

Retrieval augmented generation optimizes the output of large language models by applying more context to prompts.

Setup and configuration
The following Python modules are to be installed during this hands-on introduction.

hdbcli
The Python Database API Specification v2.0 (PEP 249) defines a set of methods that provides a consistent database interface independent of the actual database being used. The Python extension module for SAP HANA implements PEP 249. Once you install the module, you can access and change the information in SAP HANA databases from Python.

generative-ai-hub-sdk
With this SAP python SDK you can leverage the power of generative Models like chatGPT available in SAP's generative AI Hub.

Folium
Folium builds on the data wrangling strengths of the Python ecosystem and the mapping strengths of the Leaflet.js library. Manipulate your data in Python, then visualize it in a Leaflet map via folium.
