# Spark Decision Tree Classification

This Java-based Spark application demonstrates the training and testing of a Decision Tree classifier using Spark MLlib. The code is designed to load a dataset, train a Decision Tree model, and evaluate its performance on a validation dataset.

## Prerequisites

- **Apache Spark:** Ensure that you have Apache Spark installed and configured. You can download Spark from [here](https://spark.apache.org/downloads.html).

- **Java Development Kit (JDK):** Make sure you have Java installed on your system. You can download the JDK from [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).

## Project Structure

- **src/:** Contains the Java source code files.
  - `DecisionTreeSpark.java`: Code for training a Decision Tree model and evaluating it on a test dataset.
  - `TestDecisionTreeModel.java`: Code for loading a pre-trained Decision Tree model and testing it on a validation dataset.

- **data/:** Placeholder for your dataset files.
  - `TrainingDataset.csv`: Training dataset in CSV format.
  - `ValidationDataset.csv`: Validation dataset in CSV format.

- **model/:** Placeholder for storing the trained Decision Tree model.

## Running the Code

1. Ensure that Spark is correctly installed, and the `spark-submit` script is in your system's PATH.

2. Compile the Java code:

    ```bash
    javac -cp "path/to/spark/jars/*" src/*.java
    ```

3. Run the training and testing code:

    ```bash
    spark-submit --class DecisionTreeSpark --master local[*] --driver-class-path "path/to/spark/jars/*" src/DecisionTreeSpark.java
    ```

4. Run the pre-trained model testing code:

    ```bash
    spark-submit --class TestDecisionTreeModel --master local[*] --driver-class-path "path/to/spark/jars/*" src/TestDecisionTreeModel.java
    ```

## Notes

- Update dataset paths in the code if your datasets are located in a different directory.

- Update the model path in `TestDecisionTreeModel.java` to point to the directory where the trained model is saved.

- Adjust column names and configurations based on your actual dataset structure.

