## Training Models with Unequal Economic Error Costs in Amazon Sagemaker

Many companies are turning to machine learning (ML) to improve customer and business outcomes. They use the power of ML models built over "big data" to identify patterns and find correlations. Then they can identify appropriate approaches or predict likely outcomes based on data about new instances. However, all models make errors. In some applications all errors are truly equal. In other applications, one kind of error can be much more costly or consequential than another - measured in absolute or relative terms, in dollars, time, or something else.

With the code contained in this repo, we address this second kind of application. We show how to train a model in Amazon SageMaker for a binary classification problem in which the costs of different kinds of misclassification are very different. In this case, the cost of a false positive error is much smaller than the cost of a false negative error. To solve this problem, we show you how to write a custom loss function that incorporates asymmetric misclassification costs and how to train an Amazon SageMaker Build Your Own Model using that loss function. Further, we show how to evaluate the errors made by the model and how to compare models trained with different relative costs so that you can identify the model with the best economic outcome overall.

The advantage of this approach is that it makes an explicit link between an ML model's outcomes and errors and the business' framework for decision-making. This approach requires the business to explicitly state its cost matrix, based on the specific actions to be taken on the predictions. The business can then evaluate the economic consequences of the model predictions on their overall processes, the actions taken based on the predictions, and their associated costs. This evaluation process moves well beyond simply assessing the classification results of the model. This approach can drive challenging discussions in the business, and force differing implicit decisions and valuations onto the table for open discussion and agreement.

To build and train the model, open the jupyter notebook contained in the custom-loss folder and follow the instructions in the notebook.

Additionally, there is a notebook in the custom-loss folder called "Training_Models_with_Unequal_Economic_Error_Costs.ipynb" that trains the model locally and does not depend upon Sagemaker.

## License Summary

This sample code is made available under a modified MIT license. See the LICENSE file.
