// Login.tsx
import React, { useState } from 'react';
import './Login.css'; // Make sure this is correctly imported

const Login: React.FC = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = (e: React.FormEvent) => {
    e.preventDefault();
    // Handle login logic here
    console.log('Email:', email);
    console.log('Password:', password);
  };

  return (
    <div className="loginPageWrapper">
      <div className="container">
        <div className="formContainer">
          <h2 className="title">Login</h2>
          <form onSubmit={handleLogin} className="form">
            <div className="inputGroup">
              <label htmlFor="email">Email</label>
              <input
                type="email"
                id="email"
                placeholder="Enter your email"
                value={email}
                onChange={(e) => setEmail(e.target.value)}
                required
              />
            </div>

            <div className="inputGroup">
              <label htmlFor="password">Password</label>
              <input
                type="password"
                id="password"
                placeholder="Enter your password"
                value={password}
                onChange={(e) => setPassword(e.target.value)}
                required
              />
            </div>
            //
              <div className="loginPageWrapper">
      <div className="container">
        <div className="formContainer">
          <h2 className="title">Login</h2>
          <form onSubmit={handleLogin} className="form">
            <div className="inputGroup">
              <label htmlFor="email">Email</label>
              <input
                type="email"
                id="email"
                placeholder="Enter your email"
                value={email}
                onChange={(e) => setEmail(e.target.value)}
                required
              />
            </div>
            //

            <button type="submit" className="loginButton">
              Login
            </button>

            <p className="registerText">
              New here?{' '}
              <a href="/register" className="registrationLink">
                Register
              </a>
            </p>

            <p className="forgotPassword">
              <a href="/forgot-password" className="registrationLink">
                Forgot Password?
              </a>
            </p>
          </form>
        </div>
      </div>
    </div>
  );
};

export default Login;
