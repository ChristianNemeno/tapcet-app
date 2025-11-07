# UI Components

This file lists the reusable UI components (Composables) for the Nemeno Quiz App.

## Dashboard Screen

*   **`CourseCard(course: Course, progress: Float)`**: A card that displays information about a single course, including its name and the user's progress.
*   **`CourseList(courses: List<Course>)`**: A lazy list that displays all the `CourseCard` items.
*   **`UserProfileHeader(user: User)`**: A header component that shows the user's name, profile picture, and current point total.

## Quiz Screen

*   **`QuestionDisplay(question: Question)`**: A component to show the current question text.
*   **`AnswerOption(text: String, onSelected: () -> Unit)`**: A button or selectable row for a single answer choice.
*   **`QuizProgressBar(progress: Float)`**: A progress bar to show the user how far they are through the current quiz.
*   **`FeedbackDialog(isCorrect: Boolean)`**: A dialog that appears after an answer to show if it was correct or not.

## Common Components

*   **`PrimaryButton(text: String, onClick: () -> Unit)`**: A standard button for primary actions (e.g., "Start Quiz", "Next Question").
*   **`AppBar(title: String)`**: A top app bar to display the screen title and navigation icons.
*   **`LoadingSpinner()`**: A circular progress indicator to show when data is loading.
