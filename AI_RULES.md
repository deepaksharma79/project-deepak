# AI Development Rules - Fraud Detection System

## Tech Stack
- **Python 3.x**: Core language for machine learning logic and data processing.
- **Streamlit**: Current framework for the web interface and model interaction.
- **Pandas**: Primary library for data manipulation and feature engineering.
- **Joblib**: Used for loading the pre-trained machine learning pipeline (`.pkl`).
- **React (TypeScript)**: The standard for building the modern, scalable web frontend.
- **Tailwind CSS**: For utility-first styling and ensuring responsive design across all devices.
- **Shadcn/UI**: For high-quality, accessible, and consistent UI components.
- **Lucide React**: For all iconography needs within the application.

## Library Usage Rules
- **UI Components**: Use **Streamlit** for the existing dashboard. For the modern web app, use **Shadcn/UI** components exclusively.
- **Data Handling**: Use **Pandas** for all data preprocessing to ensure consistency with the model's training requirements.
- **Model Loading**: Always use **Joblib** to load `.pkl` files.
- **Frontend Logic**: Use **React Hooks** (useState, useEffect) for state management in the web application.
- **Icons**: Use **Lucide React** for all icons to maintain visual consistency.
- **Routing**: Use **React Router** for navigation, with all routes defined in `src/App.tsx`.

## Development Standards
- **File Structure**: All React source code must be in the `src/` folder. Pages go in `src/pages/` and components in `src/components/`.
- **Component Size**: Keep components small and focused, ideally under 100 lines of code.
- **Type Safety**: Use **TypeScript** for all new frontend development to ensure robust code.
- **Responsiveness**: All UI elements must be fully responsive using Tailwind CSS classes.