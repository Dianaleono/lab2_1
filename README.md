<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Криворізька міська рада - VR макет</title>
  <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
</head>
<body>
  <a-scene>
    <!-- Небо з градієнтом -->
    <a-sky color="#87CEEB"></a-sky>
    
    <!-- Попереднє завантаження текстур -->
    <a-assets>
      <img id="brick" src="https://cdn.aframe.io/a-painter/images/brick.jpg">
      <img id="bricks2" src="https://raw.githubusercontent.com/aframevr/sample-assets/master/assets/images/bricks/bricks2.jpg">
      <img id="concrete" src="https://cdn.aframe.io/360-image-gallery-boilerplate/img/city.jpg">
      <img id="grass" src="https://cdn.aframe.io/a-painter/images/grass.jpg">
    </a-assets>
    
    <!-- Основа (трава навколо будівлі) -->
    <a-plane position="0 0 0" rotation="-90 0 0" width="80" height="80" 
             material="src: #grass; repeat: 8 8"></a-plane>
    
    <!-- Асфальтові доріжки -->
    <a-plane position="0 0.01 -20" rotation="-90 0 0" width="50" height="10" color="#424242"></a-plane>
    <a-plane position="20 0.01 0" rotation="-90 0 90" width="40" height="10" color="#424242"></a-plane>
    <a-plane position="-20 0.01 0" rotation="-90 0 90" width="40" height="10" color="#424242"></a-plane>
    
    <!-- Головна будівля міської ради -->
    <a-entity id="main-building" position="0 0 0">
      
      <!-- Основний корпус (прямокутна частина) -->
      <a-box position="0 5 0" width="24" height="10" depth="16" 
             material="src: #bricks2; roughness: 0.8; repeat: 12 5; color: #D2B48C">
      </a-box>
      
      <!-- Центральна фасадна частина -->
      <a-box position="0 5 -8.5" width="20" height="10" depth="1" 
             material="src: #bricks2; roughness: 0.6; repeat: 10 5; color: #F5DEB3">
      </a-box>
      
      <!-- Колони (5 колон) -->
      <a-cylinder position="-8 5 -8.5" radius="1" height="10" 
                  material="src: #bricks2; roughness: 0.5; repeat: 2 5; color: #F5DEB3"></a-cylinder>
      <a-cylinder position="-4 5 -8.5" radius="1" height="10" 
                  material="src: #bricks2; roughness: 0.5; repeat: 2 5; color: #F5DEB3"></a-cylinder>
      <a-cylinder position="0 5 -8.5" radius="1" height="10" 
                  material="src: #bricks2; roughness: 0.5; repeat: 2 5; color: #F5DEB3"></a-cylinder>
      <a-cylinder position="4 5 -8.5" radius="1" height="10" 
                  material="src: #bricks2; roughness: 0.5; repeat: 2 5; color: #F5DEB3"></a-cylinder>
      <a-cylinder position="8 5 -8.5" radius="1" height="10" 
                  material="src: #bricks2; roughness: 0.5; repeat: 2 5; color: #F5DEB3"></a-cylinder>
      
      <!-- Дах основної будівлі -->
      <a-box position="0 10.5 0" width="26" height="1" depth="18" color="#8B4513"></a-box>
      
      <!-- Фронтон (трикутна частина даху) -->
      <a-entity position="0 12 -8.5">
        <a-cone position="0 0 0" radius-bottom="10" radius-top="0" height="4" 
                rotation="0 0 0" color="#8B4513"></a-cone>
      </a-entity>
      
      <!-- Головний вхід -->
      <a-box position="0 2.5 -9" width="5" height="5" depth="0.5" 
             material="src: #brick; color: #654321"></a-box>
      <a-box position="0 2.5 -9.2" width="4" height="4" depth="0.2" color="#2F4F4F"></a-box>
      
      <!-- Сходи (багато рівнів) -->
      <a-box position="0 0.1 -10" width="8" height="0.2" depth="2" color="#696969"></a-box>
      <a-box position="0 0.3 -10.5" width="8" height="0.2" depth="1" color="#696969"></a-box>
      <a-box position="0 0.5 -11" width="8" height="0.2" depth="1" color="#696969"></a-box>
      <a-box position="0 0.7 -11.5" width="8" height="0.2" depth="1" color="#696969"></a-box>
      <a-box position="0 0.9 -12" width="8" height="0.2" depth="1" color="#696969"></a-box>
      
      <!-- Вікна першого поверху -->
      <a-box position="-8 3 -9" width="2.5" height="2" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="8 3 -9" width="2.5" height="2" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="-6 3 -9" width="1.5" height="2" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="6 3 -9" width="1.5" height="2" depth="0.1" color="#87CEEB"></a-box>
      
      <!-- Вікна другого поверху -->
      <a-box position="-10 7 -9" width="2" height="1.5" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="-6 7 -9" width="2" height="1.5" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="6 7 -9" width="2" height="1.5" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="10 7 -9" width="2" height="1.5" depth="0.1" color="#87CEEB"></a-box>
      
      <!-- Бокові вікна -->
      <a-box position="-12.2 4 -3" width="0.1" height="2" depth="3" color="#87CEEB"></a-box>
      <a-box position="-12.2 4 3" width="0.1" height="2" depth="3" color="#87CEEB"></a-box>
      <a-box position="12.2 4 -3" width="0.1" height="2" depth="3" color="#87CEEB"></a-box>
      <a-box position="12.2 4 3" width="0.1" height="2" depth="3" color="#87CEEB"></a-box>
      
      <!-- Задні вікна -->
      <a-box position="-6 4 8.2" width="3" height="2" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="0 4 8.2" width="3" height="2" depth="0.1" color="#87CEEB"></a-box>
      <a-box position="6 4 8.2" width="3" height="2" depth="0.1" color="#87CEEB"></a-box>
      
      <!-- Прапор України -->
      <a-entity position="0 15 -4">
        <a-cylinder position="0 0 0" radius="0.15" height="5" color="#8B4513"></a-cylinder>
        <a-plane position="2 1.5 0" width="4" height="2.5" color="#005BBB" 
                 animation="property: rotation; to: 0 10 0; dur: 4000; dir: alternate; loop: true">
          <a-plane position="0 -0.625 0.01" width="4" height="1.25" color="#FFD700"></a-plane>
        </a-plane>
      </a-entity>
      
    </a-entity>
    
    <!-- Адміністративні прибудови -->
    <a-box position="-18 3 -8" width="10" height="6" depth="10" 
           material="src: #brick; roughness: 0.8; repeat: 5 3; color: #CD853F"></a-box>
    <a-box position="18 3 -8" width="10" height="6" depth="10" 
           material="src: #brick; roughness: 0.8; repeat: 5 3; color: #CD853F"></a-box>
    
    <!-- Дахи прибудов -->
    <a-box position="-18 6.5 -8" width="11" height="1" depth="11" color="#8B4513"></a-box>
    <a-box position="18 6.5 -8" width="11" height="1" depth="11" color="#8B4513"></a-box>
    
    <!-- Паркування -->
    <a-plane position="0 0.01 20" rotation="-90 0 0" width="40" height="20" color="#2F2F2F"></a-plane>
    
    <!-- Розмітка паркування -->
    <a-plane position="-12 0.02 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="-6 0.02 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="0 0.02 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="6 0.02 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="12 0.02 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    
    <!-- Дерева навколо -->
    <a-entity position="-25 0 -15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" color="#8B4513"></a-cylinder>
      <a-sphere position="0 6 0" radius="4" color="#228B22"></a-sphere>
    </a-entity>
    
    <a-entity position="25 0 -15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" color="#8B4513"></a-cylinder>
      <a-sphere position="0 6 0" radius="4" color="#228B22"></a-sphere>
    </a-entity>
    
    <a-entity position="-30 0 15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" color="#8B4513"></a-cylinder>
      <a-sphere position="0 6 0" radius="4" color="#228B22"></a-sphere>
    </a-entity>
    
    <a-entity position="30 0 15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" color="#8B4513"></a-cylinder>
      <a-sphere position="0 6 0" radius="4" color="#228B22"></a-sphere>
    </a-entity>
    
    <!-- Додаткові декоративні елементи -->
    <a-entity position="0 0 -25">
      <a-cylinder position="0 1 0" radius="0.3" height="2" color="#8B4513"></a-cylinder>
      <a-sphere position="0 2.5 0" radius="1.5" color="#228B22"></a-sphere>
    </a-entity>
    
    <a-entity position="15 0 -25">
      <a-cylinder position="0 1 0" radius="0.3" height="2" color="#8B4513"></a-cylinder>
      <a-sphere position="0 2.5 0" radius="1.5" color="#228B22"></a-sphere>
    </a-entity>
    
    <a-entity position="-15 0 -25">
      <a-cylinder position="0 1 0" radius="0.3" height="2" color="#8B4513"></a-cylinder>
      <a-sphere position="0 2.5 0" radius="1.5" color="#228B22"></a-sphere>
    </a-entity>
    
    <!-- Освітлення -->
    <a-light type="ambient" color="#ffffff" intensity="0.7"></a-light>
    <a-light type="directional" position="15 25 15" color="#ffffff" intensity="0.9"></a-light>
    <a-light type="point" position="0 10 -10" color="#ffddaa" intensity="0.5"></a-light>
    
    <!-- Текст з назвою -->
    <a-text value="КРИВОРІЗЬКА МІСЬКА РАДА" 
            position="0 1.5 -15" 
            color="#003366" 
            align="center" 
            scale="3 3 3"
            font="dejavu">
    </a-text>
    
    <!-- Анімована камера що "від'їжджає" від будівлі -->
    <a-entity id="camera-rig" position="0 8 35">
      <a-camera look-controls="enabled: true" wasd-controls="enabled: true">
        <!-- Анімація камери: обертання навколо будівлі + віддалення -->
        <a-animation attribute="position" 
                    to="0 15 60" 
                    dur="20000" 
                    repeat="indefinite"
                    direction="alternate">
        </a-animation>
        
        <!-- Анімація обертання камери -->
        <a-animation attribute="rotation" 
                    to="0 360 0" 
                    dur="40000" 
                    repeat="indefinite"
                    easing="linear">
        </a-animation>
      </a-camera>
    </a-entity>
    
    <!-- Альтернативна анімація для плавного огляду -->
    <a-entity id="orbit-camera" position="0 12 45" visible="false">
      <a-camera>
        <a-animation attribute="position" 
                    to="0 20 70" 
                    dur="30000" 
                    repeat="indefinite"
                    direction="alternate"
                    easing="easeInOutQuad">
        </a-animation>
      </a-camera>
    </a-entity>
    
  </a-scene>

  <script>
    // Додаткова логіка для перемикання між камерами
    document.addEventListener('keydown', function(event) {
      const mainCamera = document.querySelector('#camera-rig');
      const orbitCamera = document.querySelector('#orbit-camera');
      
      if (event.key === '1') {
        mainCamera.setAttribute('visible', true);
        orbitCamera.setAttribute('visible', false);
      } else if (event.key === '2') {
        mainCamera.setAttribute('visible', false);
        orbitCamera.setAttribute('visible', true);
      }
    });
  </script>
</body>
</html>
