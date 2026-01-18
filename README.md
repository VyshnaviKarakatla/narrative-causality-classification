#Narrative Consistency Classification

This project builds a machine learning system that checks whether a hypothetical character backstory is logically consistent with a full-length novel. The focus of the task is global reasoning across long narratives rather than short text understanding.

The project was developed as part of the Kharagpur Data Science Hackathon 2026.


#Project Summary
The problem involves analyzing a complete novel containing more than one hundred thousand words and a newly written backstory for a main character. The goal is to predict whether the backstory can logically produce the events and character behavior observed in the novel. If it fits, the output is Consistent. If it conflicts with the narrative, the output is Contradict.

The approach begins with cleaning the raw text by converting it to lowercase and removing unnecessary characters. Because the stories are very long, each narrative is split into smaller overlapping parts so that important context is not lost. These text parts are then converted into numerical values using TF-IDF, which highlights important words while reducing the impact of very common ones.

A Logistic Regression model is trained on these processed text chunks. Each chunk receives a prediction, and all chunk predictions belonging to the same story are combined to produce a final story-level decision. This aggregation step allows the system to reason across the entire narrative instead of relying on a single fragment.

The model achieves strong performance at both the chunk level and the story level. Final predictions for the test data are saved in a file named results.csv.

The project is implemented using Python with the Pandas, NumPy, and Scikit-learn libraries. The code is organized into a notebook for training and prediction, a report explaining the approach, and a results file containing the final outputs.

To run the project, the required Python libraries must be installed and the notebook should be executed from start to finish. The notebook reads the input data, trains the model, and generates the final prediction file automatically.

This project was completed as a solo submission by Vyshnavi Karakatla for the Kharagpur Data Science Hackathon 2026.
