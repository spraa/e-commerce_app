# YouTube Clone Application (MERN Stack)

## Overview
The **YouTube Clone Application** is a video-sharing platform built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It allows users to upload, view, and interact with videos, mimicking the core functionalities of YouTube.

## Features

- **User Authentication**: Sign up and log in using email and password.
- **Video Upload**: Upload and manage videos with metadata like title, description, and tags.
- **Video Playback**: Stream videos directly from the platform.
- **Likes and Dislikes**: Engage with videos by liking or disliking.
- **Comments**: Add, view, and delete comments on videos.
- **Subscriptions**: Subscribe to channels to receive updates on new uploads.
- **Search Functionality**: Search for videos and channels.
- **User Profiles**: View and edit profile details, including uploaded videos.

## Tech Stack

- **Frontend**: React.js, Redux (for state management)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **APIs**: Cloudinary (for video storage and streaming)
- **Authentication**: JWT (JSON Web Token)

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Node.js (v14 or higher)
- MongoDB (local or cloud-based, e.g., MongoDB Atlas)

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/youtube-clone.git
   cd youtube-clone
   ```

2. **Install Dependencies**:
   Navigate to both the `client` and `server` directories to install dependencies:
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the `server` directory with the following keys:
   ```env
   PORT=5000
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
   CLOUDINARY_API_KEY=your-cloudinary-api-key
   CLOUDINARY_API_SECRET=your-cloudinary-api-secret
   ```

4. **Run the Application**:
   - Start the backend server:
     ```bash
     cd server
     npm start
     ```
   - Start the frontend client:
     ```bash
     cd client
     npm start
     ```

5. **Access the App**:
   Open your browser and navigate to `http://localhost:3000`.

## Folder Structure

```
youtube-clone/
│
├── client/                # Frontend code
│   ├── public/            # Static files
│   ├── src/               # React app source code
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Pages for the app
│   │   ├── redux/         # Redux setup
│   │   └── App.js         # Root component
│
├── server/                # Backend code
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── controllers/       # Route handlers
│   └── server.js          # Entry point
│
└── README.md              # Documentation
```

## API Endpoints

### User Authentication
- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: Log in an existing user

### Video Management
- **POST /api/videos**: Upload a new video
- **GET /api/videos**: Fetch all videos
- **GET /api/videos/:id**: Fetch a specific video
- **PUT /api/videos/:id**: Update video details
- **DELETE /api/videos/:id**: Delete a video

### Comments
- **POST /api/videos/:id/comment**: Add a comment
- **GET /api/videos/:id/comments**: Fetch comments for a video
- **DELETE /api/comments/:id**: Delete a comment

### Engagement
- **POST /api/videos/:id/like**: Like a video
- **POST /api/videos/:id/dislike**: Dislike a video

### Subscriptions
- **POST /api/users/:id/subscribe**: Subscribe to a user
- **POST /api/users/:id/unsubscribe**: Unsubscribe from a user

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push to the branch.
5. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
- Cloudinary for video hosting and streaming.
- Open-source libraries and tools that made this project possible.
