# Overview

This is an interactive web application that demonstrates the ε-Greedy algorithm, a fundamental reinforcement learning strategy used in multi-armed bandit problems. The application is built as a single-page web application using HTML, CSS, JavaScript, and PyScript to provide an educational tool for understanding how the ε-Greedy algorithm balances exploration and exploitation in decision-making scenarios.

The application allows users to adjust key parameters (number of arms k, number of trials T, and initial epsilon value) and run simulations to see real-time visualizations of regret accumulation and optimal action percentage over time.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The application uses a client-side architecture with PyScript integration:
- **HTML Structure**: Single-page application with semantic HTML markup
- **CSS Styling**: Modern, responsive design with grid layouts and custom styling
- **PyScript Integration**: Uses PyScript 2024.1.1 for running Python code in the browser
- **Interactive Components**: Real-time controls and visualizations for algorithm demonstration

## Component Design
- **Container-based Layout**: Centered content container with responsive design
- **Grid-based Controls**: Flexible control panel using CSS Grid for parameter adjustment
- **Educational Interface**: User-friendly interface designed for learning and experimentation

## Programming Paradigm
- **Client-side Processing**: All computation happens in the browser using PyScript
- **Interactive Learning**: Real-time parameter adjustment and immediate visual feedback
- **Educational Focus**: Designed to help users understand reinforcement learning concepts

# External Dependencies

## Core Technologies
- **PyScript 2024.1.1**: Python runtime in the browser for algorithm implementation
- **Modern Web Standards**: HTML5, CSS3, and vanilla JavaScript for the user interface

## CDN Resources
- **PyScript CDN**: Hosted PyScript core files for Python execution in browser
- **Web Fonts**: Segoe UI font stack for consistent typography across platforms

## Browser Requirements
- **Modern Browser Support**: Requires browsers with WebAssembly support for PyScript
- **No Backend Dependencies**: Fully client-side application with no server requirements