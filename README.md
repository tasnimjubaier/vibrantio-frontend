# Vibrantio - Frontend

### Description
Vibrantio is a platform designed to foster team engagement and boost morale for remote teams. This repository contains the frontend code, built with **React** and **AWS Amplify** for authentication.

### Project Structure
- **React** - Component-based library for building the UI.
- **Material-UI** - For styling components and ensuring a consistent design.
- **AWS Amplify** - Integration with AWS Cognito for secure user authentication.

### Features
- **User Registration and Login** - Secure authentication with AWS Cognito.
- **Recognition System** - Allows team members to recognize and appreciate each other's contributions.
- **Wellness Check-Ins** - Users can submit their mood to help managers gauge team morale.
- **Engagement Dashboard** - An overview of recent team recognitions, morale trends, and more.

### Getting Started

#### Prerequisites
- Node.js (v14+)
- NPM or Yarn

#### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/vibrantio-frontend.git
   cd vibrantio-frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Set up AWS Amplify configuration:
   - Copy your AWS Cognito configuration to `src/aws-exports.js` with the following structure:
     ```javascript
     import Amplify from 'aws-amplify';

     Amplify.configure({
       Auth: {
         region: 'your-aws-region',
         userPoolId: 'your-cognito-user-pool-id',
         userPoolWebClientId: 'your-cognito-app-client-id',
         mandatorySignIn: true,
       },
     });
     ```

#### Running the App
To start the development server:
```bash
npm start
# or
yarn start
```
The app should be running on [http://localhost:3000](http://localhost:3000).

### Deployment
For production, we recommend deploying the app on **AWS S3** with **CloudFront** as a CDN for faster load times.

### Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes and commit (`git commit -m 'Add feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a Pull Request.

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
