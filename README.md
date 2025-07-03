<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Криворізька міська рада - 3D макет</title>
  <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
  <style>
    body { 
      margin: 0; 
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    }
    
    .info-panel {
      position: fixed;
      top: 20px;
      left: 20px;
      background: rgba(255, 255, 255, 0.95);
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      z-index: 1000;
      max-width: 300px;
    }
    
    .info-panel h2 {
      margin: 0 0 10px 0;
      color: #2c3e50;
      font-size: 18px;
    }
    
    .info-panel p {
      margin: 5px 0;
      color: #34495e;
      font-size: 14px;
    }
    
    .controls {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: rgba(0, 0, 0, 0.8);
      color: white;
      padding: 15px;
      border-radius: 10px;
      font-size: 12px;
      z-index: 1000;
    }
    
    a-scene {
      width: 100vw;
      height: 100vh;
    }
  </style>
</head>
<body>
  <div class="info-panel">
    <h2>🏛️ Криворізька міська рада</h2>
    <p><strong>Адреса:</strong> просп. Миру, 21, Кривий Ріг</p>
    <p><strong>Архітектура:</strong> Класична з елементами модерну</p>
    <p><strong>Побудовано:</strong> 1970-ті роки</p>
    <p><strong>Особливості:</strong> Центральний фасад з колонами</p>
  </div>
  
  <div class="controls">
    <strong>Управління:</strong><br>
    WASD - рух<br>
    Миша - огляд<br>
    Автообертання: 30 сек
  </div>

  <a-scene background="color: #87CEEB" fog="type: linear; color: #87CEEB; near: 50; far: 100">
    
    <!-- Освітлення -->
    <a-light type="ambient" color="#ffffff" intensity="0.7"></a-light>
    <a-light type="directional" position="20 30 20" color="#ffffff" intensity="0.9" 
             light="castShadow: true; shadowMapWidth: 2048; shadowMapHeight: 2048"></a-light>
    <a-light type="point" position="0 15 0" color="#FFD700" intensity="0.3"></a-light>
    
    <!-- Основа та навколишнє середовище -->
    <a-plane position="0 0 0" rotation="-90 0 0" width="80" height="80" 
             color="#2E7D32" 
             material="roughness: 0.8"
             shadow="receive: true">
    </a-plane>
    
    <!-- Площа перед будівлею -->
    <a-plane position="0 0.01 -20" rotation="-90 0 0" width="50" height="15" 
             color="#D2B48C" 
             material="roughness: 0.6"
             shadow="receive: true">
    </a-plane>
    
    <!-- Дороги навколо -->
    <a-plane position="0 0.02 -35" rotation="-90 0 0" width="60" height="10" color="#2F2F2F"></a-plane>
    <a-plane position="25 0.02 0" rotation="-90 0 90" width="50" height="10" color="#2F2F2F"></a-plane>
    <a-plane position="-25 0.02 0" rotation="-90 0 90" width="50" height="10" color="#2F2F2F"></a-plane>
    
    <!-- Головна будівля міської ради -->
    <a-entity id="main-building" position="0 0 0">
      
      <!-- Основний корпус -->
      <a-box position="0 5 0" width="24" height="10" depth="16" 
             color="#E6E6FA" 
             material="roughness: 0.3; metalness: 0.1"
             shadow="cast: true; receive: true">
      </a-box>
      
      <!-- Центральний фасад з колонами -->
      <a-box position="0 5 -8.5" width="20" height="10" depth="1" 
             color="#F5F5DC" 
             material="roughness: 0.2; metalness: 0.1"
             shadow="cast: true">
      </a-box>
      
      <!-- Колони (класичний стиль) -->
      <a-cylinder position="-8 5 -8.5" radius="0.6" height="10" 
                  color="#F5F5DC" 
                  material="roughness: 0.2"
                  shadow="cast: true">
      </a-cylinder>
      <a-cylinder position="-4 5 -8.5" radius="0.6" height="10" 
                  color="#F5F5DC" 
                  material="roughness: 0.2"
                  shadow="cast: true">
      </a-cylinder>
      <a-cylinder position="0 5 -8.5" radius="0.6" height="10" 
                  color="#F5F5DC" 
                  material="roughness: 0.2"
                  shadow="cast: true">
      </a-cylinder>
      <a-cylinder position="4 5 -8.5" radius="0.6" height="10" 
                  color="#F5F5DC" 
                  material="roughness: 0.2"
                  shadow="cast: true">
      </a-cylinder>
      <a-cylinder position="8 5 -8.5" radius="0.6" height="10" 
                  color="#F5F5DC" 
                  material="roughness: 0.2"
                  shadow="cast: true">
      </a-cylinder>
      
      <!-- Капітелі колон -->
      <a-box position="-8 10.2 -8.5" width="1.5" height="0.4" depth="1.5" color="#D4AF37"></a-box>
      <a-box position="-4 10.2 -8.5" width="1.5" height="0.4" depth="1.5" color="#D4AF37"></a-box>
      <a-box position="0 10.2 -8.5" width="1.5" height="0.4" depth="1.5" color="#D4AF37"></a-box>
      <a-box position="4 10.2 -8.5" width="1.5" height="0.4" depth="1.5" color="#D4AF37"></a-box>
      <a-box position="8 10.2 -8.5" width="1.5" height="0.4" depth="1.5" color="#D4AF37"></a-box>
      
      <!-- Дах -->
      <a-box position="0 11 0" width="26" height="1.5" depth="18" 
             color="#8B4513" 
             material="roughness: 0.7"
             shadow="cast: true">
      </a-box>
      
      <!-- Фронтон над входом -->
      <a-entity position="0 12 -8.5">
        <a-triangle position="0 0 0" rotation="0 0 0" 
                   geometry="primitive: triangle; vertexA: -6 0 0; vertexB: 6 0 0; vertexC: 0 4 0" 
                   material="color: #8B4513; roughness: 0.7"
                   shadow="cast: true">
        </a-triangle>
      </a-entity>
      
      <!-- Головний вхід -->
      <a-box position="0 2.5 -9" width="5" height="5" depth="0.8" 
             color="#654321" 
             material="roughness: 0.5"
             shadow="cast: true">
      </a-box>
      
      <!-- Двері -->
      <a-box position="0 2.5 -9.3" width="4" height="4.5" depth="0.2" 
             color="#2F4F4F" 
             material="roughness: 0.3; metalness: 0.2">
      </a-box>
      
      <!-- Ручки дверей -->
      <a-sphere position="1.5 2.5 -9.4" radius="0.05" color="#FFD700"></a-sphere>
      <a-sphere position="-1.5 2.5 -9.4" radius="0.05" color="#FFD700"></a-sphere>
      
      <!-- Сходи -->
      <a-box position="0 0.3 -10.5" width="8" height="0.6" depth="3" 
             color="#696969" 
             material="roughness: 0.8"
             shadow="receive: true">
      </a-box>
      <a-box position="0 0.6 -11" width="8" height="0.6" depth="2" 
             color="#696969" 
             material="roughness: 0.8"
             shadow="receive: true">
      </a-box>
      <a-box position="0 0.9 -11.5" width="8" height="0.6" depth="1" 
             color="#696969" 
             material="roughness: 0.8"
             shadow="receive: true">
      </a-box>
      
      <!-- Вікна першого поверху -->
      <a-box position="-8 3 -8.7" width="2.5" height="2" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="8 3 -8.7" width="2.5" height="2" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      
      <!-- Вікна другого поверху -->
      <a-box position="-9 7 -8.7" width="2" height="1.5" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="-5 7 -8.7" width="2" height="1.5" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="5 7 -8.7" width="2" height="1.5" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="9 7 -8.7" width="2" height="1.5" depth="0.1" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      
      <!-- Бокові вікна -->
      <a-box position="-12.2 4 -3" width="0.1" height="2" depth="3" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="-12.2 4 3" width="0.1" height="2" depth="3" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="12.2 4 -3" width="0.1" height="2" depth="3" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      <a-box position="12.2 4 3" width="0.1" height="2" depth="3" 
             color="#87CEEB" 
             material="opacity: 0.7; transparent: true">
      </a-box>
      
      <!-- Прапор України -->
      <a-entity position="0 14 -4">
        <a-cylinder position="0 0 0" radius="0.08" height="5" 
                    color="#8B4513" 
                    shadow="cast: true">
        </a-cylinder>
        <a-plane position="2 1.5 0" width="4" height="2.5" 
                 color="#005BBB" 
                 material="side: double"
                 animation="property: rotation; to: 0 10 0; dur: 4000; dir: alternate; loop: true"
                 shadow="cast: true">
          <a-plane position="0 -0.625 0.01" width="4" height="1.25" 
                   color="#FFD700" 
                   material="side: double">
          </a-plane>
        </a-plane>
      </a-entity>
      
    </a-entity>
    
    <!-- Бічні адміністративні будівлі -->
    <a-box position="-20 3 -5" width="10" height="6" depth="12" 
           color="#D2B48C" 
           material="roughness: 0.4"
           shadow="cast: true; receive: true">
    </a-box>
    <a-box position="20 3 -5" width="10" height="6" depth="12" 
           color="#D2B48C" 
           material="roughness: 0.4"
           shadow="cast: true; receive: true">
    </a-box>
    
    <!-- Дахи бічних будівель -->
    <a-box position="-20 6.5 -5" width="11" height="1" depth="13" 
           color="#8B4513" 
           shadow="cast: true">
    </a-box>
    <a-box position="20 6.5 -5" width="11" height="1" depth="13" 
           color="#8B4513" 
           shadow="cast: true">
    </a-box>
    
    <!-- Паркування -->
    <a-plane position="0 0.02 20" rotation="-90 0 0" width="40" height="20" 
             color="#2F2F2F" 
             material="roughness: 0.9"
             shadow="receive: true">
    </a-plane>
    
    <!-- Розмітка паркування -->
    <a-plane position="-12 0.03 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="-6 0.03 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="0 0.03 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="6 0.03 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    <a-plane position="12 0.03 20" rotation="-90 0 0" width="0.3" height="18" color="#FFFFFF"></a-plane>
    
    <!-- Дерева навколо -->
    <a-entity position="-30 0 -15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" 
                  color="#8B4513" 
                  shadow="cast: true">
      </a-cylinder>
      <a-sphere position="0 6 0" radius="4" 
                color="#228B22" 
                material="roughness: 0.8"
                shadow="cast: true">
      </a-sphere>
    </a-entity>
    
    <a-entity position="30 0 -15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" 
                  color="#8B4513" 
                  shadow="cast: true">
      </a-cylinder>
      <a-sphere position="0 6 0" radius="4" 
                color="#228B22" 
                material="roughness: 0.8"
                shadow="cast: true">
      </a-sphere>
    </a-entity>
    
    <a-entity position="-35 0 15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" 
                  color="#8B4513" 
                  shadow="cast: true">
      </a-cylinder>
      <a-sphere position="0 6 0" radius="4" 
                color="#228B22" 
                material="roughness: 0.8"
                shadow="cast: true">
      </a-sphere>
    </a-entity>
    
    <a-entity position="35 0 15">
      <a-cylinder position="0 2.5 0" radius="0.8" height="5" 
                  color="#8B4513" 
                  shadow="cast: true">
      </a-cylinder>
      <a-sphere position="0 6 0" radius="4" 
                color="#228B22" 
                material="roughness: 0.8"
                shadow="cast: true">
      </a-sphere>
    </a-entity>
    
    <!-- Ліхтарі -->
    <a-entity position="-15 0 -25">
      <a-cylinder position="0 4 0" radius="0.2" height="8" color="#2F2F2F"></a-cylinder>
      <a-sphere position="0 8.5 0" radius="0.8" 
                color="#FFD700" 
                material="emissive: #FFD700; emissiveIntensity: 0.3"
                light="type: point; color: #FFD700; intensity: 0.5; distance: 15">
      </a-sphere>
    </a-entity>
    
    <a-entity position="15 0 -25">
      <a-cylinder position="0 4 0" radius="0.2" height="8" color="#2F2F2F"></a-cylinder>
      <a-sphere position="0 8.5 0" radius="0.8" 
                color="#FFD700" 
                material="emissive: #FFD700; emissiveIntensity: 0.3"
                light="type: point; color: #FFD700; intensity: 0.5; distance: 15">
      </a-sphere>
    </a-entity>
    
    <!-- Назва будівлі -->
    <a-text value="КРИВОРІЗЬКА МІСЬКА РАДА" 
            position="0 1.5 -15" 
            color="#003366" 
            align="center" 
            scale="3 3 3"
            font="dejavu"
            material="shader: msdf; alphaTest: 0.5"
            animation="property: scale; to: 3.2 3.2 3.2; dur: 3000; dir: alternate; loop: true">
    </a-text>
    
    <!-- Інформаційна табличка -->
    <a-plane position="0 1.2 -14.5" width="12" height="2" 
             color="#F5F5DC" 
             material="opacity: 0.9"
             shadow="cast: true">
      <a-text value="просп. Миру, 21" 
              position="0 -0.3 0.01" 
              color="#2F4F4F" 
              align="center" 
              scale="1.5 1.5 1.5">
      </a-text>
    </a-plane>
    
    <!-- Камера з автообертанням -->
    <a-entity id="rig" position="0 8 35">
      <a-camera look-controls wasd-controls="enabled: true" 
                position="0 0 0"
                animation="property: rotation; to: 0 360 0; dur: 30000; loop: true; easing: linear">
      </a-camera>
    </a-entity>
    
  </a-scene>
</body>
</html>
