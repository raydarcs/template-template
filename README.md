/* Reset de estilos básicos */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Arial', sans-serif;
  background-color: #f8f8f8;
  color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
  overflow: hidden;
}

.container {
  position: relative;
  max-width: 600px;
  padding: 20px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  z-index: 1;
}

.carta-titulo {
  font-size: 2rem;
  color: #d72d6f;
  margin-bottom: 20px;
}

.carta p {
  font-size: 1.2rem;
  margin-bottom: 10px;
  line-height: 1.6;
}

.coracao-container {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
  pointer-events: none;
  z-index: 0;
}

.coracao {
  width: 50px;
  height: 50px;
  background-color: #ff4081;
  clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 20% 100%, 0% 35%);
  animation: flutuar 5s infinite ease-in-out;
  cursor: pointer;
}

.coracao:hover {
  animation: explosao 0.6s forwards;
}

@keyframes flutuar {
  0% {
    transform: translateY(0) scale(1);
  }
  50% {
    transform: translateY(-30px) scale(1.2);
  }
  100% {
    transform: translateY(0) scale(1);
  }
}

@keyframes explosao {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.5);
    opacity: 0.8;
  }
  100% {
    transform: scale(0);
    opacity: 0;
  }
}

audio {
  display: none;
}
