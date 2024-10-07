# Student Answer Script Evaluation Model
This repository contains a model designed to automate the process of evaluating student answer scripts. By leveraging NLP (Natural Language Processing) and machine learning techniques, the model provides feedback and predicted grades based on the quality and relevance of the student's response. This automation aims to alleviate the burden on teachers, allowing them to focus more on lesson planning and teaching.

## Features
- **BERT for Text Classification**: Utilizes a pre-trained BERT model for sequence classification to assess the relevance and correctness of student answers.
- **Grammar Check**: Implements basic grammar mistake detection using POS tagging.
- **Keyword Matching**: Checks for key concepts and relevant points in student responses.
- **Point-based Scoring**: Assigns scores based on the presence of required points in the answers.
- **Feedback System**: Provides dynamic feedback based on the score, encouraging students to improve their answers.

## Requirements
To run the notebook, you'll need the following libraries:
- `torch`
- `transformers`
- `scikit-learn`
- `nltk`

You can install the required dependencies by running:

```bash
!pip install torch torchvision transformers scikit-learn nltk
```

## How It Works
1. **Preprocessing**: Student answers are preprocessed using a stemmer to normalize the text.
2. **Keyword Matching**: The model checks for key terms related to the question in the student's response.
3. **Grammar Analysis**: Uses part-of-speech tagging to detect basic grammar patterns and flag mistakes.
4. **Point-based Scoring**: Assigns a score based on the number of valid points made in the answer.
5. **Feedback Generation**: Feedback is generated dynamically, offering insights into how well the student performed and suggesting areas for improvement.

## Example Usage
```python
# Sample keywords for the question
keywords_for_question = ["supervised", "unsupervised", "learning"]
point_based_question = True

# Input: Student's answer
student_answer = input("Enter your response: ")

# Get feedback and score
feedback, score = get_feedback(student_answer, keywords_for_question, point_based_question)

# Output predicted score and feedback
print(f"Predicted Grade: {score}")
print("Feedback:", feedback)
```

Example Output:
```
Enter your response: Unsupervised learning:- No help at all is provided, the model should learn everything on its own, Supervised learning:- Humans oversee and help the model to learn
Predicted Grade: 1
Feedback: Good job! You've covered some of the main points.
```

## Contributing
Feel free to fork this repository, raise issues, or submit pull requests if you have suggestions for improving the model or its implementation.

## License
This project is open-source and available under the [MIT License](LICENSE).


Let me know if you'd like any modifications to this!
