# Overview 

The goal of this assignment is to assess your understanding of how to design a sequence diagram based on scenario description. 

# Instructions

Create a UML use case diagram (using PlantUML syntax) for the following scenario:

Users of a simple question-and-answer app can submit questions that must begin with either:

* "What should I do to...", or
* "What should I do if..."

When a question is submitted, the frontend sends it to the backend, which uses Natural Language Processing (NLP) to standardize the question text. The backend then queries a curated database of answers to popular questions. If an answer is found, it is returned to the frontend. If no answer is found, the backend responds with:

* "Hmmm... Let me think about it. Ask me again in 24 hours."

The question is then saved in the database for future review.

Periodically, human editors review unanswered questions in the database. After conducting research, they write responses—often with a touch of humor and sarcasm—which are then stored in the database.

Whenever a response is sent to the user, the frontend also contacts the ad server to request a new advertisement. The ad is displayed alongside the answer. This is how the app generates revenue.

The app promises to answer all questions within 24 hours, provided they do not violate the usage policy, which prohibits questions involving criminal or offensive content.

Required participants:

* User
* Frontend
* Backend
* Database
* Ad Server

The diagram should include:

* The frontend displaying an input form for the user to enter a question.
* The backend processing the question and querying the database.
* An alternative flow showing:
    * One path where an answer is found and returned.
    * Another path where no answer is found, a placeholder response is returned, and the question is saved.
* A message exchange between the frontend and the ad server to retrieve an ad before displaying the final response to the user.

Use the provided [scenario.wsd](scenario.wsd) file.
