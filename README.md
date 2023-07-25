# Fake-Review-Detection
To view the user's portfolio blog on the Fake Review Detection, please visit [My Blog](https://danielrs.systeme.io/fake-review-detection) to see the explanation of the notebook.

Due to the use of `plotly.express` and `plotly.graph_objects`, the visualizations in this code cannot be displayed on GitHub. To view the visualizations, please download the code and run it on your local machine.

## Dataset Information
Here is a table with the columns and their descriptions for the `review_data` DataFrame:

| Column   | Description                                                  |
|----------|--------------------------------------------------------------|
| category | The category of the product being reviewed.                  |
| rating   | The rating given by the reviewer (on a scale of 1 to 5).      |
| label    | The label assigned to the review (either "OR = Original Review" or "CG = Computer-generated").   |
| text_    | The text of the review.                                      |

Note that the `text_` column has an underscore at the end of its name, which may be a typo. If you want to access this column, you should use `review_data['text_']` instead of `review_data['text']`. The generated fake reviews dataset, containing 20k fake reviews and 20k real product reviews. `OR = Original reviews` (presumably human created and authentic); `CG = Computer-generated` fake reviews. For building the model, we only require two columns: `"text_"` (containing the review text) and `"label"` (indicating whether the review is authentic or BOT-generated). The "text_" column will serve as the input data for the model, while the "label" column will be the target variable that the model needs to predict. The labels will typically be binary, with "1" representing BOT-generated reviews and "0" representing authentic reviews.

## Usage

Here is a table with the files in the directory and their descriptions:

| File name                | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Fake Review Detection.ipynb | A Jupyter Notebook containing code and analysis for detecting fake reviews. |
| LICENSE                  | The license file for the project.                                           |
| README.md                | The README file for the project.                                             |
| dt.pkl                   | A saved decision tree model for detecting fake reviews.                     |
| fake reviews dataset.csv | The dataset of reviews used for training and testing the models.            |
| gitattributes            | A Git configuration file for handling line endings.                         |
| lr.pkl                   | A saved logistic regression model for detecting fake reviews.               |
| nb.pkl                   | A saved Naive Bayes model for detecting fake reviews.                        |
| svm.pkl                  | A saved support vector machine model for detecting fake reviews.            |
| vectorizer.pickle        | A saved TfidfVectorizer object for transforming text data into vectors.     |

## Dataset Source

You can get the data from [Fake Review Dataset](https://osf.io/tyue9/).

First click here![image](https://github.com/armans28/Fake-Review-Detection/assets/119162844/402cb97f-b218-46eb-8f19-fb900550b598)

After that, click here ![image](https://github.com/armans28/Fake-Review-Detection/assets/119162844/c0915208-66be-4e4d-8042-6017a6a23641)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
