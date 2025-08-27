<h1 align="center">🖐️ PROJETO - HAND TRACKING</h1> <p align="center"> <img src="https://github.com/user-attachments/assets/02c81cc4-3811-451d-94b8-46af6aab4f9d" alt="Hand Tracking Banner" width="100%"/> </p>

<p align="center"> 	
<a href="https://www.canva.com/pt_br/"><img src="https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white"/></a> 
<a href="https://www.raspberrypi.com/software/"><img src="https://img.shields.io/badge/-RaspberryPi-C51A4A?style=for-the-badge&logo=Raspberry-Pi"/></a> 
<a href="https://www.notion.so/pt-br"><img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white"/></a> 
<a href="https://opencv.org/"><img src="https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white"/></a> 
<a href="https://ai.google.dev/edge/mediapipe/solutions/guide?hl=pt-br"><img src="https://img.shields.io/badge/MediaPipe-00BFAE?style=for-the-badge&logo=mediapipe&logoColor=white"/></a> 
<a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue"/></a>
<a href="https://code.visualstudio.com/"><img src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"/></a> 
</p>

<h1>🎯 Objetivo do Projeto</h1> 
<p> Este projeto visa detectar movimentos da mão em tempo real utilizando uma webcam conectada ao Raspberry Pi 5. Através das bibliotecas <strong>OpenCV</strong>, <strong>MediaPipe</strong> e <strong>gpiod</strong>, o sistema reconhece quais dedos estão levantados e aciona LEDs conectados aos pinos GPIO conforme o gesto captado. </p> <p> Por exemplo: se o usuário levantar três dedos, três LEDs se acendem. O projeto demonstra uma forma simples e eficaz de interação gestual para automação física. </p>

<h1>📦 Materiais Utilizados</h1> 
<h3>🖥️ Equipamentos</h3> 
<ul> 
	<li>Raspberry Pi 5</li> 
	<li>Webcam Logitech C920s PRO HD</li> 
	<li>TV</li> <li>Notebook</li> <li>Sinaleira</li> 
	<li>Fonte 24V</li> </ul> <h3>💻 Software</h3> 
 <ul> 
	 <li>VS Code</li> 
 </ul> 
 <h3>🔌 Hardware</h3> 
 <ul> 
	 <li>GPIO</li> 
 </ul> 
 <h3>🧠 Linguagens e Bibliotecas</h3>
 <ul> 
	 <li>Python</li> 
	 <li>OpenCV</li> 
	 <li>MediaPipe</li> 
 </ul>

<h1>🍓 Raspberry Pi 5</h1> 
<p>🔗 Site oficial: <a href="https://www.raspberrypi.com/" target="_blank">raspberrypi.com</a></p> 
<p> O <strong>Raspberry Pi</strong> é um microcomputador compacto que permite o desenvolvimento de projetos educacionais e de automação. </p> 

<p align="center"> <img src="https://github.com/user-attachments/assets/64cf2ded-cc0d-40cf-9a69-ac18ea12f3cf" width="60%"> </p>

<h3>🔽 1. Instalação do Sistema Operacional</h3> 
<p>Utilize o <strong>Raspberry Pi Imager</strong>:</p> 
<ul> 
	<li>Baixe em: <a href="https://www.raspberrypi.com/software/">raspberrypi.com/software</a></li> 
	<li>Escolha o sistema (ex: Raspberry Pi OS)</li> <li>Selecione o cartão microSD</li> 
	<li>Configure Wi-Fi e nome do host (opcional)</li> <li>Clique em "Write" e aguarde a finalização</li> 
</ul> 
<p align="center"><img src="https://github.com/user-attachments/assets/37aa2b46-9433-4acd-bf1e-47e2f48ad0f4" width="60%"></p>

<h1>🐍 Python</h1> 

<p>🔗 Site oficial: <a href="https://www.python.org/" target="_blank" rel="noopener noreferrer">python.org</a></p> 
<p>Este guia passo a passo mostra como configurar um ambiente virtual Python para seu projeto, garantindo isolamento e organização das dependências.</p>
<h3>📁 1. Criar a Pasta do Projeto e o Ambiente Virtual</h3> 
<p>Abra o terminal (Prompt de Comando, PowerShell, Terminal Linux ou macOS) e execute os comandos abaixo para criar a pasta do projeto e o ambiente virtual:</p> 
<pre lang="bash">
<code> 
#Cria uma pasta para o projeto e entra nela 
mkdir meu_projeto cd meu_projeto 
<br>
#Cria o ambiente virtual chamado "venv" 
python -m venv venv 
</code>
</pre> 
<p>O ambiente virtual "venv" cria uma instalação isolada do Python para seu projeto, evitando conflitos com outras bibliotecas instaladas globalmente.</p>
<h3>🔌 2. Ativar o Ambiente Virtual</h3> 
<p>Depois de criar o ambiente, é necessário ativá-lo para começar a usar as bibliotecas instaladas dentro dele. O comando varia conforme seu sistema operacional:</p> 
<h4><img src="https://img.icons8.com/color/20/000000/windows-11.png" width="20" alt="Windows"/> Windows:</h4> 
<pre lang="powershell">
<code>
venv\Scripts\activate 
</code>
</pre> 
<h4>🍎 macOS / 🐧 Linux:</h4> 
<pre lang="bash">
<code> 
source venv/bin/activate
</code>
</pre> 
<p>Ao ativar, seu terminal deve mostrar o nome do ambiente entre parênteses, indicando que o ambiente virtual está ativo:</p> 
<pre lang="bash">
<code>
(venv) user@pc:~/meu_projeto$
</code>
</pre>
<h3>📦 3. Instalar as Bibliotecas Necessárias</h3> 
<p>Com o ambiente ativado, você pode instalar as bibliotecas que seu projeto precisa usando o 
<code>pip</code>. Por exemplo, para instalar o OpenCV e o MediaPipe:</p> 
<pre lang="bash">
<code>
pip install opencv-python mediapipe 
</code>
</pre>
<h3>✅ 4. Verificação da Instalação</h3> 
<p>Para garantir que tudo está funcionando corretamente, crie um arquivo Python (por exemplo, <code>test.py</code>) com o seguinte código ou execute diretamente no terminal interativo:</p> 
<pre lang="python">
<code>
import cv2 
import mediapipe as mp 
<br>
print("OpenCV versão:", cv2.__version__) 
print("MediaPipe importado com sucesso!") 
</code>
</pre> 

<p>Se a saída mostrar a versão do OpenCV e a mensagem de sucesso do MediaPipe, sua configuração está pronta para uso!</p>

<h1>👨‍💻 Código Final</h1>

### O código completo detecta quais dedos estão levantados e aciona os pinos GPIO correspondentes para controlar os LEDs.

<pre lang="python"><code>
import cv2
import mediapipe as mp
import gpiod
import math
import time
<br>
#Pinos GPIO para os 5 relés (polegar até mindinho)
rele_pins = [14, 15, 18, 23, 24]
chip = gpiod.Chip('gpiochip0')
<br>
#Configuração dos pinos GPIO
rele_lines = []
for pin in rele_pins:
    rele_line = chip.get_line(pin)
    rele_line.request(consumer='hand_tracking', type=gpiod.LINE_REQ_DIR_OUT)
    rele_lines.append(rele_line)
<br>
#Inicializa estados anteriores dos relés
estado_rele_anterior = [0, 0, 0, 0, 0]
<br>
#MediaPipe Hands
mp_hands = mp.solutions.hands
hands = mp_hands.Hands(static_image_mode=False, max_num_hands=1, min_detection_confidence=0.5)
mp_draw = mp.solutions.drawing_utils
<br>
#Estilo leve para desenhar os pontos e conexões da mão
estilo_ponto = mp_draw.DrawingSpec(color=(0, 255, 0), thickness=1, circle_radius=1)
estilo_linha = mp_draw.DrawingSpec(color=(0, 0, 255), thickness=1)
<br>
#Captura de vídeo com resolução reduzida
cap = cv2.VideoCapture(0)
cap.set(cv2.CAP_PROP_FRAME_WIDTH, 480)
cap.set(cv2.CAP_PROP_FRAME_HEIGHT, 360)
cap.set(cv2.CAP_PROP_FPS, 30)
<br>
#Detectar resolução da tela
screen_width = 1024
screen_height = 768
<br>
#Configura a janela para tela cheia
cv2.namedWindow("Hand Tracking", cv2.WND_PROP_FULLSCREEN)
cv2.setWindowProperty("Hand Tracking", cv2.WND_PROP_FULLSCREEN, cv2.WINDOW_FULLSCREEN)

def distancia(p1, p2):
    return math.hypot(p1[0] - p2[0], p1[1] - p2[1])

def detectar_dedos_vetorial(lm_list):
    dedos = []
    
    #Verifica o ângulo entre os segmentos dos dedos
    def dedo_estendido(p1, p2, p3):
        v1 = (p2[0] - p1[0], p2[1] - p1[1])
        v2 = (p3[0] - p2[0], p3[1] - p2[1])
        dot = v1[0]*v2[0] + v1[1]*v2[1]
        norm1 = math.hypot(v1[0], v1[1])
        norm2 = math.hypot(v2[0], v2[1])
        cos_angle = dot / (norm1 * norm2 + 1e-6)
        angle = math.acos(min(1, max(-1, cos_angle)))
        return angle < math.radians(30)  # menor que ~30 graus

    #Polegar: usa landmarks 2 (base), 3 (meio), 4 (ponta)
    dedos.append(int(dedo_estendido(lm_list[2], lm_list[3], lm_list[4])))

    #Indicador, Médio, Anelar, Mindinho
    dedos.append(int(dedo_estendido(lm_list[5], lm_list[6], lm_list[8])))   # indicador
    dedos.append(int(dedo_estendido(lm_list[9], lm_list[10], lm_list[12]))) # médio
    dedos.append(int(dedo_estendido(lm_list[13], lm_list[14], lm_list[16])))# anelar
    dedos.append(int(dedo_estendido(lm_list[17], lm_list[18], lm_list[20])))# mindinho

    return dedos

frame_count = 0
fps_target = 30
tempo_por_frame = 1.0 / fps_target

while True:
    start_time = time.time()

    success, img = cap.read()
    img = cv2.flip(img, 1)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    results = hands.process(img_rgb)
    dedos = [0, 0, 0, 0, 0]

    if results.multi_hand_landmarks and results.multi_handedness:
        handLms = results.multi_hand_landmarks[0]
        hand_label = results.multi_handedness[0].classification[0].label

        lm_list = []
        for lm in handLms.landmark:
            h, w, _ = img.shape
            lm_list.append((int(lm.x * w), int(lm.y * h)))

        dedos = detectar_dedos_vetorial(lm_list)

        #Desenhar landmarks
        mp_draw.draw_landmarks(
            img,
            handLms,
            mp_hands.HAND_CONNECTIONS,
            estilo_ponto,
            estilo_linha
        )

        #Mostrar numeração dos dedos levantados
        dedo_nomes = ['1', '2', '3', '4', '5']
        pontas_dedos = [4, 8, 12, 16, 20]

        for i, idx in enumerate(pontas_dedos):
            if dedos[i]:  
                x, y = lm_list[idx]
                cv2.putText(img, dedo_nomes[i], (x - 10, y - 5), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (0, 0, 0), 4)
                cv2.putText(img, dedo_nomes[i], (x - 10, y - 5), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (255, 255, 255), 2)

    #Atualiza relés com base no estado dos dedos
    for i in range(5):
        if dedos[i] != estado_rele_anterior[i]:
            rele_estado = 0 if dedos[i] == 1 else 1 
            rele_lines[i].set_value(rele_estado)
            estado_rele_anterior[i] = dedos[i]

    if frame_count % 10 == 0:
        print("Dedos levantados:", dedos)
    frame_count += 1

    frame_fullscreen = cv2.resize(img, (screen_width, screen_height), interpolation=cv2.INTER_LINEAR)
    cv2.imshow("Hand Tracking", frame_fullscreen)

    key = cv2.waitKey(1)
    if key == 27 or key == ord('q'):
        break

    #Aguarda o tempo restante para manter 30 FPS
    elapsed = time.time() - start_time
    time_to_wait = tempo_por_frame - elapsed
    if time_to_wait > 0:
        time.sleep(time_to_wait)
<br>
#Cleanup
cap.release()
cv2.destroyAllWindows()
for rele_line in rele_lines:
    rele_line.release()
</code></pre>

<h1>🧑‍🤝‍🧑 Equipe</h1>
<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/ccadu86">
        <img src="https://avatars.githubusercontent.com/u/36140205?v=4" width="115px" alt="Carlos Eduardo"/><br />
        <sub><b>Carlos Eduardo</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/MatheusGatto78">
        <img src="https://avatars.githubusercontent.com/u/176522380?v=4" width="115px" alt="Matheus Gatto"/><br />
        <sub><b>Matheus Gatto</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/gabibuenorosa">
        <img src="https://avatars.githubusercontent.com/u/176522402?v=4" width="115px" alt="Matheus Gatto"/><br />
        <sub><b>Gabriela Bueno</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Luizavm">
        <img src="https://avatars.githubusercontent.com/u/170521509?v=4" width="115px" alt="Matheus Gatto"/><br />
        <sub><b>Luiza Vilhena</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/pribero">
        <img src="https://avatars.githubusercontent.com/u/90459377?v=4" width="115px" alt="Matheus Gatto"/><br />
        <sub><b>Pedro Ribeiro</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/ofernandesz">
        <img src="https://avatars.githubusercontent.com/u/161597028?v=4" width="115px" alt="Matheus Gatto"/><br />
        <sub><b>Caio Fernandes</b></sub>
      </a>
    </td>
  </tr>
</table>

<h1>🚀 Possíveis Expansões</h1> 
<ul> 
	<li>Controle de robôs com gestos</li> 
	<li>Automação residencial (acender luzes com a mão)</li> 
	<li>Interface sem toque para acessibilidade</li> 
</ul>
<h1>🧠 Aprendizados</h1> 
<ul> 
	<li>Integração entre software e hardware usando GPIO</li> 
	<li>Processamento de imagem com MediaPipe</li> 
	<li>Uso de Python para prototipagem rápida</li>
</ul>
<h1>🤝 Colaboração</h1>
<p>Agradecemos ao Professor Leo por todo apoio durante o trabalho, nos ajudando na criação das placas e em possiveis idéias</p>

<br>

<details>
  <summary>Click here to the English version</summary>

  <h1 align="center">🖐️ PROJECT - HAND TRACKING WITH RASPBERRY PI 5</h1> 
<p align="center"> <img src="https://github.com/user-attachments/assets/02c81cc4-3811-451d-94b8-46af6aab4f9d" alt="Hand Tracking Banner" width="100%"/> </p> 
<p align="center"> 
  <a href="https://www.canva.com/"><img src="https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white"/></a> 
  <a href="https://www.raspberrypi.com/software/"><img src="https://img.shields.io/badge/-RaspberryPi-C51A4A?style=for-the-badge&logo=Raspberry-Pi"/></a> 
  <a href="https://www.notion.so/"><img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white"/></a> 
  <a href="https://opencv.org/"><img src="https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white"/></a> 
  <a href="https://ai.google.dev/edge/mediapipe/solutions/guide"><img src="https://img.shields.io/badge/MediaPipe-00BFAE?style=for-the-badge&logo=mediapipe&logoColor=white"/></a> 
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue"/></a> 
  <a href="https://code.visualstudio.com/"><img src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white"/></a> 
</p>

<h1>🎯 Project Objective</h1>
This project aims to detect hand gestures in real-time using a webcam connected to a Raspberry Pi 5. Using OpenCV, MediaPipe, and gpiod, the system recognizes raised fingers and activates LEDs connected to GPIO pins accordingly.

Example: If the user raises three fingers, three LEDs will light up. This demonstrates a simple and effective way of gesture-based physical interaction.

<h1>📦 Materials Used</h1>
<h3>🖥️ Equipment</h3>

<ul>
  <li>Raspberry Pi 5</li>
  <li>Logitech C920s PRO HD Webcam</li>
  <li>TV</li>
  <li>Laptop</li>
  <li>LED Signal Tower</li>
  <li>24V Power Supply</li>
</ul>

<h3>💻 Software</h3>

<ul>
  <li>Visual Studio Code</li>
</ul>

<h3>🔌 Hardware</h3>

<ul>
  <li>GPIO</li>
</ul>

<h3>🧠 Languages & Libraries</h3>

<ul>
  <li>Python</li>
  <li>OpenCV</li>
  <li>MediaPipe</li>
</ul>

<h1>🍓 Raspberry Pi 5</h1>
🔗 Official website: <a href="raspberrypi.com">raspberrypi.com</a>

The Raspberry Pi is a compact microcomputer that enables the development of educational and automation projects.

<p align="center"> <img src="https://github.com/user-attachments/assets/64cf2ded-cc0d-40cf-9a69-ac18ea12f3cf" width="60%"> </p>

<h3>🔽 1. Installing the OS</h3>
Use the Raspberry Pi Imager:

Download from: <a href="raspberrypi.com/software">raspberrypi.com/software</a>

Choose the OS (e.g., Raspberry Pi OS)

Select the microSD card

Optionally set Wi-Fi and hostname

Click "Write" and wait for the process to complete

<p align="center"> <img src="https://github.com/user-attachments/assets/37aa2b46-9433-4acd-bf1e-47e2f48ad0f4" width="60%"> </p>
<h1>🐍 Python</h1>
🔗 Official website: <a href="python.org">python.org</a>

A step-by-step guide to setting up a virtual Python environment for better project organization.

<h3>📁 1. Create Project Folder and Virtual Environment</h3>

<pre lang="bash">
<code>
# Create the project folder and enter it
mkdir my_project
cd my_project
<br>
# Create the virtual environment named "venv"
python -m venv venv
</code>
</pre>

🔌 2. Activate the Virtual Environment

<h3><img src="https://img.icons8.com/color/48/windows-11.png" alt="Windows 11" width="20" height="20"> Windows:</h3>

<pre lang="bash">
<code>
venv\Scripts\activate
</code>
</pre>

<h3>🍎 macOS / 🐧 Linux:</h3>

<pre lang="bash">
<code>
source venv/bin/activate
</code>
</pre>

Once activated, your terminal will show (venv) indicating it's active:

<pre lang="bash">
<code>
(venv) user@pc:~/my_project$
</code>
</pre>

📦 3. Install Required Libraries
With the environment active, install the needed libraries:

<pre lang="python">
<code>
pip install opencv-python mediapipe
</code>
</pre>

✅ 4. Verify Installation
Create a test.py file and run:

<pre lang="python">
<code>
import cv2
import mediapipe as mp
<br>
print("OpenCV version:", cv2.__version__)
print("MediaPipe successfully imported!")
</code>
</pre>

If no errors appear, you're ready!

<h1>👨‍💻 Final Code</h1>
The final script detects raised fingers and activates the corresponding GPIO pins to control LEDs.
<pre lang="python"><code>
import cv2
import mediapipe as mp
import gpiod
import math
import time
<br>
#Pinos GPIO para os 5 relés (polegar até mindinho)
rele_pins = [14, 15, 18, 23, 24]
chip = gpiod.Chip('gpiochip0')
<br>
#Configuração dos pinos GPIO
rele_lines = []
for pin in rele_pins:
    rele_line = chip.get_line(pin)
    rele_line.request(consumer='hand_tracking', type=gpiod.LINE_REQ_DIR_OUT)
    rele_lines.append(rele_line)
<br>
#Inicializa estados anteriores dos relés
estado_rele_anterior = [0, 0, 0, 0, 0]
<br>
#MediaPipe Hands
mp_hands = mp.solutions.hands
hands = mp_hands.Hands(static_image_mode=False, max_num_hands=1, min_detection_confidence=0.5)
mp_draw = mp.solutions.drawing_utils
<br>
#Estilo leve para desenhar os pontos e conexões da mão
estilo_ponto = mp_draw.DrawingSpec(color=(0, 255, 0), thickness=1, circle_radius=1)
estilo_linha = mp_draw.DrawingSpec(color=(0, 0, 255), thickness=1)
<br>
#Captura de vídeo com resolução reduzida
cap = cv2.VideoCapture(0)
cap.set(cv2.CAP_PROP_FRAME_WIDTH, 480)
cap.set(cv2.CAP_PROP_FRAME_HEIGHT, 360)
cap.set(cv2.CAP_PROP_FPS, 30)
<br>
#Detectar resolução da tela
screen_width = 1024
screen_height = 768
<br>
#Configura a janela para tela cheia
cv2.namedWindow("Hand Tracking", cv2.WND_PROP_FULLSCREEN)
cv2.setWindowProperty("Hand Tracking", cv2.WND_PROP_FULLSCREEN, cv2.WINDOW_FULLSCREEN)

def distancia(p1, p2):
    return math.hypot(p1[0] - p2[0], p1[1] - p2[1])

def detectar_dedos_vetorial(lm_list):
    dedos = []
    
    #Verifica o ângulo entre os segmentos dos dedos
    def dedo_estendido(p1, p2, p3):
        v1 = (p2[0] - p1[0], p2[1] - p1[1])
        v2 = (p3[0] - p2[0], p3[1] - p2[1])
        dot = v1[0]*v2[0] + v1[1]*v2[1]
        norm1 = math.hypot(v1[0], v1[1])
        norm2 = math.hypot(v2[0], v2[1])
        cos_angle = dot / (norm1 * norm2 + 1e-6)
        angle = math.acos(min(1, max(-1, cos_angle)))
        return angle < math.radians(30)  # menor que ~30 graus

    #Polegar: usa landmarks 2 (base), 3 (meio), 4 (ponta)
    dedos.append(int(dedo_estendido(lm_list[2], lm_list[3], lm_list[4])))

    #Indicador, Médio, Anelar, Mindinho
    dedos.append(int(dedo_estendido(lm_list[5], lm_list[6], lm_list[8])))   # indicador
    dedos.append(int(dedo_estendido(lm_list[9], lm_list[10], lm_list[12]))) # médio
    dedos.append(int(dedo_estendido(lm_list[13], lm_list[14], lm_list[16])))# anelar
    dedos.append(int(dedo_estendido(lm_list[17], lm_list[18], lm_list[20])))# mindinho

    return dedos

frame_count = 0
fps_target = 30
tempo_por_frame = 1.0 / fps_target

while True:
    start_time = time.time()

    success, img = cap.read()
    img = cv2.flip(img, 1)
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    results = hands.process(img_rgb)
    dedos = [0, 0, 0, 0, 0]

    if results.multi_hand_landmarks and results.multi_handedness:
        handLms = results.multi_hand_landmarks[0]
        hand_label = results.multi_handedness[0].classification[0].label

        lm_list = []
        for lm in handLms.landmark:
            h, w, _ = img.shape
            lm_list.append((int(lm.x * w), int(lm.y * h)))

        dedos = detectar_dedos_vetorial(lm_list)

        #Desenhar landmarks
        mp_draw.draw_landmarks(
            img,
            handLms,
            mp_hands.HAND_CONNECTIONS,
            estilo_ponto,
            estilo_linha
        )

        #Mostrar numeração dos dedos levantados
        dedo_nomes = ['1', '2', '3', '4', '5']
        pontas_dedos = [4, 8, 12, 16, 20]

        for i, idx in enumerate(pontas_dedos):
            if dedos[i]:  
                x, y = lm_list[idx]
                cv2.putText(img, dedo_nomes[i], (x - 10, y - 5), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (0, 0, 0), 4)
                cv2.putText(img, dedo_nomes[i], (x - 10, y - 5), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (255, 255, 255), 2)

    #Atualiza relés com base no estado dos dedos
    for i in range(5):
        if dedos[i] != estado_rele_anterior[i]:
            rele_estado = 0 if dedos[i] == 1 else 1 
            rele_lines[i].set_value(rele_estado)
            estado_rele_anterior[i] = dedos[i]

    if frame_count % 10 == 0:
        print("Dedos levantados:", dedos)
    frame_count += 1

    frame_fullscreen = cv2.resize(img, (screen_width, screen_height), interpolation=cv2.INTER_LINEAR)
    cv2.imshow("Hand Tracking", frame_fullscreen)

    key = cv2.waitKey(1)
    if key == 27 or key == ord('q'):
        break

    #Aguarda o tempo restante para manter 30 FPS
    elapsed = time.time() - start_time
    time_to_wait = tempo_por_frame - elapsed
    if time_to_wait > 0:
        time.sleep(time_to_wait)
<br>
#Cleanup
cap.release()
cv2.destroyAllWindows()
for rele_line in rele_lines:
    rele_line.release()
</code></pre>

<h1>🧑‍🤝‍🧑 Team</h1>
<table align="center"> 
  <tr> 
    <td align="center"> 
      <a href="https://github.com/ccadu86"> 
      <img src="https://avatars.githubusercontent.com/u/36140205?v=4" width="115px" alt="Carlos Eduardo"/>
        <br> 
        <sub><b>Carlos Eduardo</b></sub> 
      </a> </td> <td align="center"> 
        <a href="https://github.com/MatheusGatto78"> 
          <img src="https://avatars.githubusercontent.com/u/176522380?v=4" width="115px" alt="Matheus Gatto"/>
          <br> 
          <sub><b>Matheus Gatto</b></sub>
        </a> 
    </td> 
    <td align="center"> 
      <a href="https://github.com/gabibuenorosa"> 
      <img src="https://avatars.githubusercontent.com/u/176522402?v=4" width="115px" alt="Gabriela Bueno"/>
        <br> 
        <sub><b>Gabriela Bueno</b></sub> 
      </a> 
    </td> 
    <td align="center"> 
      <a href="https://github.com/Luizavm"> 
      <img src="https://avatars.githubusercontent.com/u/170521509?v=4" width="115px" alt="Luiza Vilhena"/>
        <br> 
        <sub><b>Luiza Vilhena</b></sub> 
      </a> </td> <td align="center"> 
        <a href="https://github.com/pribero">
        <img src="https://avatars.githubusercontent.com/u/90459377?v=4" width="115px" alt="Pedro Ribeiro"/>
          <br> 
          <sub><b>Pedro Ribeiro</b></sub> 
        </a> </td> <td align="center"> 
          <a href="https://github.com/ofernandesz"> 
            <img src="https://avatars.githubusercontent.com/u/161597028?v=4" width="115px" alt="Caio Oliveira"/>
            <br> 
            <sub><b>Caio Oliveira</b></sub> 
          </a> 
        </td> 
  </tr> 
</table>

<h1>🚀 Future Expansions</h1>
Gesture-based robot control

Smart home automation (turning on lights with gestures)

Touchless interfaces for accessibility

<h1>🧠 Learnings</h1>
Software and hardware integration using GPIO

Image processing with MediaPipe

Rapid prototyping with Python

<h1>🤝 Acknowledgments</h1>
Special thanks to Professor Leo for the guidance, support with PCB creation, and helping generate new ideas for the project.

</details>
