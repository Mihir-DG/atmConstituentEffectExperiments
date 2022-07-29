## John Snow Labs Pipeline Modifications

This is in reference to the Colab notebook "JSLCopy2"; a copy of this notebook is marked in this directory, but must be recreated in the Google Colab environment for licensing reasons. The relevant code cells are listed here, in the order they appear in the notebook:

1. Cell 3 - Licensing: This requires a Spark license to be input, using the Google Colab file uploader; a regular JSON parser does not seem to update environment keys appropriately

2. Cell 7 - Package Installer: Needs to be run in order to set up spark on Colab.

3. Cell 8 - Spark Setup: Sets up the PySpark environment on Colab, with resource management taken care of.

4. Cell 10 - Pipeline setup: Used to define models used in pipeline; currently set to ner_drugs NER model; setup takes care of word embeddings installation

5. Cell 17 - Internal code: Runs the model on every line in all input files separately, returning a compiled list of entities;


### Basic Directory Structure:

Restarting runtimes in Colab eliminates local files/variables. Therefore, every time you want to run the model, all of the above cells need to be run, in that order. Additionally, the default directory structure for data we have used is described here:

1. License JSON - this is directed to /content/sample_data/ automatically - no interference is required.
