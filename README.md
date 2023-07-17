Project Overview
This project contains a Python script that analyses corpus data in JSON format. The output of the code will produce another JSON file containing the following information:
•	An entry per lemma for all lemmas in the raw data file.
•	The part of speech label and all inflection information per lemma.
•	A total frequency count for each lemma.
•	A total frequency count for each word-form per lemma.
Dependencies
The Python script requires Python 3.7 or higher. The script makes use of the built-in libraries `json`, `typing`, and `dataclasses`. 
Python Script Overview
The Python script takes as input an annotated corpus file in the JSON format that contains a list of sentences and each sentence contains a list of tokens and their corresponding syntactic and morphological information. This Python script, then, performs the following operations:
•	Imports necessary libraries and modules.
•	Defines the Lemma class: This class has corresponding fields for the string representation of the lemma itself, its part of speech, its inflections, its overall frequency, and a dictionary of word-form frequencies.
•	Defines a function that processes the raw input data. The raw data is stored as a dictionary in the input JSON file. Then the code initializes an empty dictionary to hold lemma data. It then loops over each sentence in the input data, and within each sentence, it loops over each token.
•	For each token, the script extracts the lemma, the word-form, the POS (part of speech) and the inflectional information.
•	The script then checks if the lemma has already been added to the lemma dictionary. If not, it creates a new Lemma object and adds it to the dictionary.
•	The code, then, increments the frequency counts of the lemma. The code also checks if the word-form has already been added to the word-form frequency dictionary of the lemma. If not, it adds it. Then it increments the frequency count of the word-form.
•	Thus, the output JSON file contains the information about each unique lemma in the input JSON file, information about each lemma’s POS label, inflection information and total frequency count. The output code also stores and counts the total frequency of each of the word-forms associated with a specific unique lemma.
•	Lastly, the ‘main’ function handles file input and output. The ‘asdict’ function from the dataclasses module has been used to convert each Lemma object into a dictionary that can be written to a JSON file.
Deployment
The script could potentially be deployed on a cloud-based server environment, like AWS Lambda, Google Cloud Functions, or Azure Functions, wrapped within a lightweight REST API for easy access. However, I must admit that my understanding of these cloud services is rudimentary at best. However, I am keen to learn and expand my knowledge on this subject.
Author
Md Wasim Odud

