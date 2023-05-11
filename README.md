<!DOCTYPE html>
<!--Model Information:
* title:	Jake The Dog
* source:	https://sketchfab.com/3d-models/jake-the-dog-f8a17c174f244e11af1fb668895ddcae
* author:	Arnau Azorin (https://sketchfab.com/azorin)

Model License:
* license type:	CC-BY-NC-SA-4.0 (http://creativecommons.org/licenses/by-nc-sa/4.0/)
* requirements:	Author must be credited. No commercial use. Modified versions must have the same license.

If you use this 3D model in your project be sure to copy paste this credit wherever you share it:
This work is based on "Jake The Dog" (https://sketchfab.com/3d-models/jake-the-dog-f8a17c174f244e11af1fb668895ddcae) 
by Arnau Azorin (https://sketchfab.com/azorin) licensed under CC-BY-NC-SA-4.0 (http://creativecommons.org/licenses/by-nc-sa/4.0/)
-->
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>20233099 조상혁</title>
    <style>
      h1 {
        display: inline-block;
        vertical-align: middle;
        color: white;
        margin: 0.5rem;
        padding: 0;
      }

      nav {
        display: inline-block;
        vertical-align: middle;
        float: right;
      }

      ul {
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
      }

      li.icon {
        flex-basis: 25%;
      }

      header {
        background: cadetblue;
        padding: 50px;
      }

      a {
        display: block;
        text-align: center;
        margin: 0.25rem;
        padding: 0.5rem 1rem;
        text-decoration: none;
        font-weight: bold;
        color: white;
        background: teal;
      }

      a1 {
        display: block;
        text-align: center;
        margin: 0.25rem;
        padding: 0.5rem 1rem;
        text-decoration: none;
        font-weight: bold;
        color: white;
        background: rgb(59, 111, 224);
      }

      a:hover {
        background: yellowgreen;
      }

      a1:hover {
        background: rgb(57, 230, 201);
      }

      html {
        box-sizing: border-box;
      }

      *,
      *:before,
      *:after {
        box-sizing: inherit;
      }
      .canvas {
        width: 150px;
        height: 150px;
      }
      .layout {
        max-width: auto;
        margin: 0 auto;
        padding: 20px;
        display: flex;
        flex-wrap: nowrap;
        gap: 1em;
      }
      aside {
        flex-basis: 160px;
        flex-grow: 0;
        flex-shrink: 0;
        background-color: #8ab7f2;
        color: rgb(4, 141, 77);
        margin: 0 auto;
      }
      article {
        flex-basis: 680px;
        flex-grow: 1;
        flex-shrink: 1;
        background-color: #ffe0e0;
      }
      .flexbox {
        display: flex;
        flex-wrap: wrap;
        gap: 1em;
        padding: 100px;
        background: linear-gradient(0deg, yellow, lightGreen);
      }
      .item {
        min-height: 150px;
        flex-basis: 100px;
        flex-shrink: 1;
        flex-grow: 1;
      }
      .item2 {
        min-height: 50px;
        flex-basis: auto;
        flex-shrink: 1;
        flex-grow: 1;
      }
      .btn1 {
        display: block;
        text-align: center;
        margin: 0.25rem;
        padding: 0.5rem 1rem;
        text-decoration: none;
        font-weight: bold;
        color: white;
        background: teal;
      }
    </style>
  </head>
  <body>
    <header>
      <h1>20233099 조상혁</h1>
      <nav>
        <ul>
          <li><a href="click_animate1">자기소개</a></li>
          <li><a href="#" onclick="click_animate2();">프로필</a></li>
          <li><a onclick="animate();">연락처</a></li>
        </ul>
      </nav>
    </header>
    <div class="layout">
      <aside>
        <h1>추천 사이트</h1>
        <li><a1 href="https://wink.kookmin.ac.kr/">Wink </a1></li>
        <li><a1 href="https://openai.com/blog/chatgpt">chat-gpt </a1></li>
        <li>
          <a1 href="https://www.daleseo.com/css-align-right/">참고 사이트 1</a1>
        </li>
        <li><a1 href="https://blogpack.tistory.com/862">참고 사이트2</a1></li>
      </aside>

      <article>
        <div class="flexbox">
          <div class="item">
            <h2>자기소개</h2>
            <p>안녕하세요!</p>
            <p>저는 이번 2023학년도 윙크에 들어오게된 조상혁입니다.</p>
            <p>아직 부족한 점이 많지만 동아리에서 활동하며</p>
            <p>부족한 점들을 채우고 싶습니다!</p>
          </div>
          <div class="item">
            <h2>프로필</h2>
            <p>2004.04.19</p>
            <p>오동초등학교 졸</p>
            <p>충의중학교 졸</p>
            <p>송양고등학교 졸</p>
            <p>국민대학교 재학중</p>
            <p>동아리 wink</p>
          </div>
          <div class="item">
            <h2>연락처</h2>
            <p>010-8863-1728</p>
          </div>
          <canvas id="canvas"></canvas>
        </div>
      </article>
    </div>

    <script type="importmap">
      {
        "imports": {
          "three": "https://unpkg.com/three@0.141.0/build/three.module.js",
          "OrbitControls": "https://unpkg.com/three@0.141.0/examples/jsm/controls/OrbitControls.js",
          "GLTFLoader": "https://unpkg.com/three@0.141.0/examples/jsm/loaders/GLTFLoader.js"
        }
      }
    </script>

    <script type="module">
      import * as THREE from 'three';
      import { GLTFLoader } from 'GLTFLoader';
      import { OrbitControls } from 'OrbitControls';

      let scene = new THREE.Scene();
      let renderer = new THREE.WebGLRenderer({
        canvas: document.querySelector('#canvas'),
        antialias: true,
      });
      renderer.outputEncoding = THREE.sRGBEncoding;

      let camera = new THREE.PerspectiveCamera(30, 1);
      camera.position.set(5, 10, 20);

      scene.background = new THREE.Color('#87CEEB');

      let ambientLight = new THREE.AmbientLight(0xffffff, 0.9); // 환경광 추가
      scene.add(ambientLight);

      let loader = new GLTFLoader();
      loader.load('bmo/scene.gltf', function (gltf) {
        scene.add(gltf.scene);

        let controls = new OrbitControls(camera, renderer.domElement);

        function animate() {
          requestAnimationFrame(animate);
          gltf.scene.rotation.y -= 0.01;
          renderer.render(scene, camera);
        }
        animate();
      });
    </script>
  </body>
</html>
