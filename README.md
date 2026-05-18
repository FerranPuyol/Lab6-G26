# Lab6-G26
Prompt 1:
Create a React application for a survey management system. Set up the main App.jsx component with the following structure:
- A header with the app title "App d'Enquestes"
- A role switcher (dropdown) to toggle between "Administrador" and "Usuari" roles
- A main content area that will render different views
- Use useState to manage: current view (list/create/answer/results), current role, and a surveys array with one sample survey
- The sample survey should have a title, an array of questions (each with text and options array), and a responses array

Use only React hooks, no external libraries.

Prompt 2:
In App.jsx, implement the survey list view (when view === 'list'). It should:
- Show each survey as a card with: title, number of questions badge, number of responses badge
- If role is "Administrador": show buttons "Resultats", "Duplicar" and "Eliminar" for each survey
- If role is "Usuari": show a "Respondre" button for each survey
- If role is "Administrador": show a "Nova enquesta" button at the top that sets view to 'create'
- Duplicating a survey should create a copy with title + " (còpia)" and empty responses array
- Deleting should remove the survey from the array
- After duplicating or deleting, show a confirmation message (alert or inline message)

Prompt 3:
Add the "create" view to the survey app. When view === 'create', show a form where 
the administrator can:
- Enter a survey title (text input)
- Add questions, each with a text field and at least 2 answer options (text inputs)
- Add more options to each question with an "Afegir opció" button
- Add more questions with an "Afegir pregunta" button
- Remove individual questions and options
- Save the survey with a "Crear enquesta" button (validates all fields are filled, 
  adds it to the surveys array, shows confirmation message and returns to list view)
- Cancel with a "Cancel·lar" button that returns to list view

Prompt 4:
Add the "answer" view to the survey app. When view === 'answer', show the selected 
survey questions so the user can answer them anonymously. It should:
- Show an info message saying responses are anonymous
- Show each question with radio buttons for each option
- Only enable the submit button when all questions are answered
- On submit, save the responses to the survey's responses array
- Show a thank you confirmation message after submitting
- Include a "Tornar" button to go back to the list view

Prompt 5:
Add the "results" view to the survey app. When view === 'results', show the 
statistics of the selected survey. It should:
- Show a summary with total number of questions and total responses
- For each question, show a progress bar for each option with the number of 
  responses and percentage
- If there are no responses yet, show a message saying so
- Include a "Tornar" button to go back to the list view

Prompt 6:
Improve the visual design of the survey app. Keep all functionality intact but upgrade the styles:
- Add a clean navbar with a logo icon and the app title
- Use a modern color palette with a primary blue (#1a56db) and soft backgrounds
- Improve cards with subtle shadows and hover effects
- Style badges with different colors (questions in blue, responses in green)
- Make buttons more polished with rounded corners and smooth transitions
- Improve the progress bars in the results view with rounded ends and a gradient fill
- Add a footer with the app name
- Make the overall layout feel more professional and modern