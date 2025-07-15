
# YouTube Clone - Backend

This is the backend server for the YouTube Clone project. It handles user authentication, video upload and management, channel creation, and interactions such as likes, comments, and subscriptions.

## Technologies Used

- Node.js
- Express.js
- MongoDB (Mongoose)
- Cloudinary (for media storage)
- Multer (for file uploads)
- JSON Web Tokens (JWT)
- dotenv

## Setup Instructions

git hub repo link : https://github.com/Akash1112003/youtube-backend

### 1. Clone the Repository



```bash
git clone https://github.com/Akash1112003/youtube-backend.git
cd youtube-backend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Variables

Create a `.env` file in the root directory and add the following:

```

MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

You can also add these in your Render/hosting provider environment settings if not using a `.env` file.

### 4. Run the Server

```bash
npm start
```

### 5. API Endpoints Overview

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and receive a JWT token
- `POST /api/channel/create` - Create a channel (requires token)
- `POST /api/upload/video` - Upload a video (requires token)
- `GET /api/videos/channel/:channelId` - Get all videos by channel
- `GET /api/video/:videoId` - Get a video by ID
- `PUT /api/video/edit/:videoId` - Edit a video (requires token)
- `DELETE /api/video/delete/:videoId` - Delete a video (requires token)
- `POST /api/upload/avatar` - Upload a channel avatar


 VErcel link :    https://youtube-frontend-theta-one.vercel.app


 ### Routes

**You can use the following routes in your frontend**

1. Signup route - `api/user/signup`
2. Login route - `api/user/signin`  
3. Upload video route - `api/video/upload`
4. Get videos route - `api/videos`  
5. Get user videos route - `api/videos/channel/:channelId`  
6. Get video route - `api/video/:videoId`
7. Delete video route - `api/video/delete/:videoId`  
8. Edit video route - `api/video/edit/:videoId`
9. Get channel route - `api/channel/:handle` 
10. Get channels route - `api/channel`  
11. Get channel videos route - `api/videos/channel/:channelId`  <
12. Create comment route - `api/comment/create/:videoId`
13. Get comments route - `api/comments/:videoId`
14. Edit comment route - `api/comment/edit/:videoId`
15. Delete comment route - `api/comment/delete/:commentId`
16. Like video route - `api/video/like/:videoId`
17. Unlike video route - `api/video/unlike/:videoId`
18. Dislike video route - `api/video/dislike/:videoId`
19. Undislike video route - `api/video/undodislike/:videoId`
20. Subscribe channel route - `api/channel/subscribe/:channelId`
21. Unsubscribe channel route - `api/channel/unsubscribe/:channelId`
22. Upload avatar route - `api/upload/avatar`
23. Upload banner route - `api/upload/banner/:channelId`
24. Increase view count route - `api/video/view/:videoId` 

| Route | Method | Signin Required |
| --- | --- | --- |
| `api/user/signup` | POST | No |
| `api/user/signin` | POST | No |
| `api/user` | GET | Yes | 
| `api/channel/create` | POST | Yes |  
| `api/channel/:handle` | GET | No |
| `api/channel` | GET | Yes |  
| `api/channelbyid/:id` | GET | No | 
| `api/video/upload` | POST | Yes |
| `api/video/:videoId` | GET | No |
| `api/videos` | GET | No |
| `api/videos/channel/:channelId` | GET | Yes |
| `api/video/delete/:videoId` | DELETE | Yes |
| `api/video/edit/:videoId` | PUT | Yes |
| `api/comment/create/:videoId` | POST | Yes |
| `api/comments/:videoId` | GET | No |
| `api/comment/edit/:videoId` | PUT | Yes |
| `api/comment/delete/:commentId` | DELETE | Yes |
| `api/video/like/:videoId` | POST | Yes |
| `api/video/unlike/:videoId` | DELETE | Yes |
| `api/video/dislike/:videoId` | POST | Yes |
| `api/video/undodislike/:videoId` | DELETE | Yes |
| `api/channel/subscribe/:channelId` | POST | Yes |
| `api/channel/unsubscribe/:channelId` | DELETE | Yes |
| `api/upload/avatar` | POST | Yes |
| `api/upload/banner/:channelId` | POST | Yes |
| `api/video/view/:videoId` | GET | No |  



## Folder Structure

```
.
├── controllers
├── middleware
├── model
├── routes
├── uploads
├── config
└── server.js
```

## Deployment

This app is deployed using Render. Ensure that all environment variables are added to Render's dashboard.


