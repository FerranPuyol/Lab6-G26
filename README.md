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

- 
