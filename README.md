<svg width="800" height="400" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Twinkling animation -->
    <animate id="twinkle1" attributeName="opacity" values="0.3;1;0.3" dur="2s" repeatCount="indefinite"/>
    <animate id="twinkle2" attributeName="opacity" values="0.5;1;0.5" dur="1.5s" repeatCount="indefinite"/>
    <animate id="twinkle3" attributeName="opacity" values="0.2;0.8;0.2" dur="2.5s" repeatCount="indefinite"/>
    
    <!-- Movement animations -->
    <animateTransform id="moveRight1" attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="15s" repeatCount="indefinite"/>
    <animateTransform id="moveRight2" attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="20s" repeatCount="indefinite"/>
    <animateTransform id="moveLeft1" attributeName="transform" type="translate" values="810,0;-10,0;810,0" dur="18s" repeatCount="indefinite"/>
    <animateTransform id="moveDown1" attributeName="transform" type="translate" values="0,-10;0,410;0,-10" dur="12s" repeatCount="indefinite"/>
    <animateTransform id="moveUp1" attributeName="transform" type="translate" values="0,410;0,-10;0,410" dur="16s" repeatCount="indefinite"/>
    <animateTransform id="moveDiag1" attributeName="transform" type="translate" values="-10,-10;810,410;-10,-10" dur="25s" repeatCount="indefinite"/>
    <animateTransform id="moveDiag2" attributeName="transform" type="translate" values="810,-10;-10,410;810,-10" dur="22s" repeatCount="indefinite"/>
  </defs>
  
  <!-- Black background -->
  <rect width="100%" height="100%" fill="#000000"/>
  
  <!-- Moving stars with different sizes and animations -->
  
  <!-- Large stars -->
  <circle cx="100" cy="80" r="1.5" fill="white">
    <animate attributeName="opacity" values="0.4;1;0.4" dur="2.2s" begin="0s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="20s" begin="0s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="300" cy="150" r="1.5" fill="white">
    <animate attributeName="opacity" values="0.3;0.9;0.3" dur="1.8s" begin="0.5s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="810,0;-10,0;810,0" dur="18s" begin="1s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="500" cy="200" r="1.5" fill="white">
    <animate attributeName="opacity" values="0.5;1;0.5" dur="2.5s" begin="1s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,-10;0,410;0,-10" dur="15s" begin="2s" repeatCount="indefinite"/>
  </circle>
  
  <!-- Medium stars -->
  <circle cx="150" cy="250" r="1" fill="white">
    <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.5s" begin="0.2s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,-10;810,410;-10,-10" dur="24s" begin="0s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="400" cy="300" r="1" fill="white">
    <animate attributeName="opacity" values="0.4;1;0.4" dur="2s" begin="1.5s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="810,-10;-10,410;810,-10" dur="22s" begin="1s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="650" cy="100" r="1" fill="white">
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="3s" begin="0.8s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="16s" begin="0.5s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="200" cy="350" r="1" fill="white">
    <animate attributeName="opacity" values="0.5;0.9;0.5" dur="1.7s" begin="2s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,410;0,-10;0,410" dur="14s" begin="1.5s" repeatCount="indefinite"/>
  </circle>
  
  <!-- Small stars -->
  <circle cx="75" cy="120" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.2;0.6;0.2" dur="2.8s" begin="0.3s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="810,0;-10,0;810,0" dur="19s" begin="0.2s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="320" cy="180" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.9s" begin="1.2s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="17s" begin="2s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="580" cy="270" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.4;0.7;0.4" dur="2.3s" begin="0.7s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,-10;0,410;0,-10" dur="13s" begin="1s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="720" cy="320" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.1;0.5;0.1" dur="3.2s" begin="1.8s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,410;0,-10;0,410" dur="21s" begin="0.5s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="450" cy="50" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.3;0.6;0.3" dur="1.6s" begin="2.5s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,-10;810,410;-10,-10" dur="26s" begin="1.2s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="120" cy="320" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.2;0.8;0.2" dur="2.1s" begin="0.9s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="810,-10;-10,410;810,-10" dur="23s" begin="2.2s" repeatCount="indefinite"/>
  </circle>
  
  <!-- Additional scattered stars for density -->
  <circle cx="250" cy="90" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.3;0.7;0.3" dur="2.4s" begin="1.3s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="-10,0;810,0;-10,0" dur="18s" begin="0.8s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="680" cy="220" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.2;0.6;0.2" dur="2.9s" begin="0.4s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,-10;0,410;0,-10" dur="16s" begin="1.7s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="380" cy="370" r="1" fill="white">
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="1.4s" begin="2.1s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="810,0;-10,0;810,0" dur="20s" begin="0.3s" repeatCount="indefinite"/>
  </circle>
  
  <circle cx="50" cy="280" r="0.5" fill="white">
    <animate attributeName="opacity" values="0.1;0.4;0.1" dur="3.5s" begin="1.6s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,410;0,-10;0,410" dur="19s" begin="2.3s" repeatCount="indefinite"/>
  </circle>
  
  <!-- Shooting star effect -->
  <line x1="700" y1="50" x2="730" y2="80" stroke="white" stroke-width="1" opacity="0">
    <animate attributeName="opacity" values="0;1;0" dur="0.5s" begin="5s;15s;25s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,0;-750,300;0,0" dur="0.5s" begin="5s;15s;25s" repeatCount="indefinite"/>
  </line>
  
  <line x1="100" y1="300" x2="130" y2="330" stroke="white" stroke-width="1" opacity="0">
    <animate attributeName="opacity" values="0;1;0" dur="0.4s" begin="10s;20s;30s" repeatCount="indefinite"/>
    <animateTransform attributeName="transform" type="translate" values="0,0;600,-250;0,0" dur="0.4s" begin="10s;20s;30s" repeatCount="indefinite"/>
  </line>
</svg>
