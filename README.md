# EduGenie-Gemini-Learning-Assistant
import os
import streamlit as st
from google import genai
from dotenv import load_dotenv

# Load environment variables
load_dotenv()

# Get Gemini API key
api_key = os.getenv("GEMINI_API_KEY")

# Check API key
if not api_key:
    st.error("Gemini API key is not configured.")
    st.info("Please create a .env file and add your GEMINI_API_KEY.")
    st.stop()

# Create Gemini client
client = genai.Client(api_key=api_key)

# Page configuration
st.set_page_config(
    page_title="EduGenie",
    page_icon="🎓",
    layout="centered"
)

# Title
st.title("🎓 EduGenie")
st.subheader("Google Gemini Powered Learning Assistant")

st.write(
    "EduGenie is an AI-powered learning assistant that helps "
    "students understand educational topics in simple language."
)

# Sidebar
st.sidebar.title("📚 EduGenie Features")

feature = st.sidebar.selectbox(
    "Choose a learning mode",
    [
        "Ask a Question",
        "Explain a Topic",
        "Create Summary",
        "Generate Quiz",
        "Create Study Notes"
    ]
)

# User input
question = st.text_area(
    "Enter your question or topic:",
    placeholder="Example: Explain Data Structures in simple English"
)

# Generate button
if st.button("✨ Generate Answer"):

    if question.strip() == "":
        st.warning("Please enter a question or topic.")
    else:

        # Different prompts for different modes
        if feature == "Ask a Question":
            prompt = f"""
            You are EduGenie, an educational AI assistant.

            Answer the student's question clearly and accurately.

            Question:
            {question}

            Use simple English and give examples when useful.
            """

        elif feature == "Explain a Topic":
            prompt = f"""
            You are EduGenie, a student-friendly AI tutor.

            Explain the following topic in simple English.

            Topic:
            {question}

            Include:
            1. Definition
            2. Main points
            3. Simple example
            4. Short conclusion
            """

        elif feature == "Create Summary":
            prompt = f"""
            You are EduGenie, an educational assistant.

            Create a short and easy-to-understand summary
            of the following topic:

            {question}

            Use important points and simple language.
            """

        elif feature == "Generate Quiz":
            prompt = f"""
            You are EduGenie, a quiz generator for students.

            Create 5 multiple-choice questions about:

            {question}

            Give four options for each question.
            Provide the correct answer after each question.
            """

        else:
            prompt = f"""
            You are EduGenie, a study-notes assistant.

            Create clear study notes for:

            {question}

            Include:
            - Definition
            - Important points
            - Examples
            - Key terms
            - Quick revision points
            """

        try:
            with st.spinner("EduGenie is thinking..."):

                response = client.models.generate_content(
                    model="gemini-3.8-flash",
                    contents=prompt
                )

                st.success("Answer generated successfully!")
                st.markdown(response.text)

        except Exception as e:
            st.error("Something went wrong.")
            st.write(str(e))

# Footer
st.divider()

st.caption(
    "EduGenie – Google Gemini Powered Learning Assistant | "
    "Educational Project"
)