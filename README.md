# CodeSync

CodeSync is a modern web application built with Next.js and React that streamlines the interview scheduling and live coding experience. It integrates a powerful code editor with real-time collaboration features, interview management, video streaming, and secure authentication. Powered by Convex for scalable backend data handling and Clerk for secure user authentication, CodeSync provides a seamless experience for candidates, interviewers, and administrators alike.

------------------------------------------------------------

## Introduction

CodeSync is designed for organizations looking to conduct efficient technical interviews. The application includes features to schedule interviews, manage candidates and interviewers, review detailed interview recordings, and solve coding questions using an in-browser Monaco code editor. By combining several cutting-edge libraries and frameworks, CodeSync delivers a modern, responsive, and intuitive user interface while leveraging serverless functions for rapid backend operations.

------------------------------------------------------------

## Features

- Interview Management:

  • Schedule new interviews with details such as title, description, date, and time  

  • Assign candidates and interviewers using dynamic selection inputs  

  • Update interview status with actions for passing or failing candidates

- Real-Time Coding Environment:

  • Integrated Monaco Editor for a smooth coding experience  

  • Multi-language support (JavaScript, Python, Java) with starter codes for various coding challenges  

  • Responsive layout with resizable panels and scroll areas

- Video and Recording Integration:

  • Built-in support for live video calls using Stream’s video SDK  

  • Automatic recording management with playback and copy-to-clipboard functionality

- User Authentication and Role Management:

  • Secure authentication using Clerk  

  • Automatic user synchronization and role assignment (candidate, interviewer)

- Backend as a Service via Convex:

  • Fully integrated Convex server functions for queries and mutations  

  • Schema definitions for users, interviews, and comments ensuring data integrity  

  • Indexing on crucial fields for faster database operations

------------------------------------------------------------

## Requirements

Before running CodeSync, ensure you have the following installed:

| Software | Minimum Version |
| --- | --- |
| Node.js | 14.x or later |
| npm or yarn | Latest |
| Next.js | 13.x or later |

Other requirements include API keys and environment variables for Convex, Clerk, and Stream Video integration.

------------------------------------------------------------

## Installation

Follow the steps below to set up the project locally:

1. Clone the repository:

```plaintext
   git clone https://github.com/priyanshujain2004/codesync.git
   cd codesync
```

1. Install dependencies:

```plaintext
   npm install
```

1. Set up environment variables:

   Create a <code>.env.local</code> file at the root of the project and add the following keys:

```plaintext
   NEXT_PUBLIC_CONVEX_URL=<your_convex_url>
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=<your_clerk_publishable_key>
   STREAM_SECRET_KEY=<your_stream_secret_key>
   NEXT_PUBLIC_STREAM_API_KEY=<your_stream_api_key>
```

1. Start the development server:

```plaintext
   npm run dev
```

------------------------------------------------------------

## Usage

Once the project is running, users can access CodeSync via their browser. The application includes several key pages:

- Dashboard:

  Manage and view upcoming interviews, update statuses, and add comments on completed sessions.

- Interview Scheduling:

  Create a new interview by selecting a candidate, adding interviewers, and specifying details like date and time.

- Live Coding and Code Editor:

  Access the integrated code editor to work through coding questions in multiple languages. The editor supports dynamic language switching and resizable panels for a flexible user experience.

- Authentication Flow:

  New users are automatically synchronized to the database via Convex functions, and role-based access is enforced using Clerk authentication.

------------------------------------------------------------

## Configuration

The project relies on several configuration files:

- Next.js and Tailwind CSS:

  The <code>next.config.mjs</code> file sets up Next.js options. Tailwind configuration in the project enhances CSS styling with a modern and responsive design.

- Convex Backend:

  All backend functions reside in the <code>convex/</code> folder. Schema definitions in <code>convex/schema.ts</code> are responsible for tables related to users, interviews, and comments.  

  For server functions, refer to files like <code>convex/users.ts</code>, <code>convex/interviews.ts</code>, and <code>convex/comments.ts</code>.

- Authentication and Providers:

  The integration with Clerk and Stream is configured in provider files under <code>src/components/providers/</code> (for example, <code>ConvexClerkProvider.tsx</code> and <code>StreamClientProvider.tsx</code>).

Adjust these configurations as necessary by editing the respective files and updating the environment variables.

------------------------------------------------------------

## Contributing

Contributions are welcome! To help improve CodeSync, please follow these guidelines:

1. Fork the Repository:

   Create your own fork and clone it locally.

1. Create a Feature Branch:

   Use a descriptive name for your branch, such as <code>feature/interview-ui-improvements</code> or <code>bugfix/login-issue</code>.

1. Commit and Push Changes:

   Make sure your code follows the project’s style guidelines and best practices. Include clear commit messages detailing the changes.

1. Submit a Pull Request:

   Once your changes are ready, open a pull request explaining the changes and why they should be merged.

1. Issue Tracking:

   Report bugs and discuss enhancements via issues on GitHub. Your suggestions are highly appreciated.

------------------------------------------------------------

## License

This project is licensed under the MIT License. Use, modify, and distribute as permitted by the terms of the license.
