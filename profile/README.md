<div align="center">
  
  # 🍙 Bab-Al 🍙 
  **AI-based Healthy Eating Habits Management Platform**  
  
  <br>
  <img src="https://github.com/user-attachments/assets/ed8c04ef-7b31-4ec4-b3ba-c794927d6fe5" alt="로고" width="200">   

  2024.03.06 ~ 2024.11.29
</div>

<br>

## Project Overview
### 📦 AI NutriTrack
- 🥗 **Nutritional Analysis**: Identify ingredients from food photos.
- 🍳 **Recipe Recommendations**: Personalized suggestions based on user preferences.
- 📊 **Health Tracking**: Graphs for better dietary management.
- 🤝 **Raspberry Pi Integration**: Meal logging for elderly and caregivers.
<br>

### 🤒 Motivation
<table>
  <tr>
    <td width="70%"><img src="https://github.com/user-attachments/assets/f907903b-d5e3-4578-92ff-7edc0457832f"></td>
    <td width="30%">
      <ul>
        <li><b>Digital Culture Impact</b></li>
        <li><b>Nutritional Imbalance</b></li>
        <li><b>Healthy Eating Focus</b></li>
        <li><b>Caregiver Support</b></li>
      </ul>
    </td>
  </tr>
</table>

<br>

### 🎯 Target
**1. 🍎 Healthy Eating Habits** : Promotes balanced diets and supports individuals aiming for long-term health improvements  
**2. 🧓 Patients or Elderly** : Assists physically challenged individuals and helps caregivers effectively manage dietary needs

<br>

### 🌌 Flow Chart
<div align="center">
  <img src="https://github.com/user-attachments/assets/8dc4bfbb-e954-4f69-aa61-66541d962fb5" width="80%">
</div>

<br>

## Techniques
### 🔧 Tools

| **Category**    | **Technologies**                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------|
| **AI**          | ![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![TensorFlow](https://img.shields.io/badge/-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white) ![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) |
| **Frontend**     | ![Swift](https://img.shields.io/badge/-Swift-FA7343?style=flat-square&logo=swift&logoColor=white) ![Xcode](https://img.shields.io/badge/-Xcode-1575F9?style=flat-square&logo=xcode&logoColor=white) |
| **Backend**      | ![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Java](https://img.shields.io/badge/-Java-007396?style=flat-square&logo=java&logoColor=white) ![AWS](https://img.shields.io/badge/-AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Embedded System** | ![Raspberry Pi](https://img.shields.io/badge/-Raspberry%20Pi-A22846?style=flat-square&logo=raspberry-pi&logoColor=white) ![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=white) ![Linux](https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black) |
| **Others**        | ![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white) ![VS Code](https://img.shields.io/badge/-VS%20Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white) ![IntelliJ IDEA](https://img.shields.io/badge/-IntelliJ%20IDEA-000000?style=flat-square&logo=intellij-idea&logoColor=white) ![Colab](https://img.shields.io/badge/-Colab-F9AB00?style=flat-square&logo=google-colab&logoColor=white) ![ngrok](https://img.shields.io/badge/-ngrok-1F1E1F?style=flat-square&logo=ngrok&logoColor=white) |

<br>

### 🛠️ Architecture
<div align="center">
  <img src="https://github.com/user-attachments/assets/ed0908ef-8279-45b1-bd40-10c7820664a1">
</div>

<br>

### 🧶 Algorithm
#### 1. Raspberry Pi Kernel Module for Camera
<table>
  <tr>
    <td>
      <p align="center">
        <img src="https://github.com/user-attachments/assets/3f8d51cd-f4b3-4041-8442-aa5d9424afeb" width="80%">
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <ul>
        <li>When the user presses a button, the connected <strong>Raspberry Pi</strong> takes a picture using the <strong>camera module</strong>.</li>
        <li>The captured image is automatically sent to our <strong>AI server</strong> for processing.</li>
        <li>The detected food name and nutritional information are then sent to our <strong>backend server</strong> via a POST request.</li>
        <li>Consequently, the user's family or caregivers can view the meal records through our <strong>iOS app</strong>.</li>
      </ul>
    </td>
  </tr>
</table>

#### 2. Food Object Detection & Nutrient Estimation
<table>
  <tr>
    <td>
      <p align="center">
        <img src="https://github.com/user-attachments/assets/01842f63-0a77-46db-bf57-fb42e1c8a274" width="80%">
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <ul>
        <li>The received image file is resized to <strong>640x640px</strong>, and the filename is modified to include the current time.</li>
        <li>The image is saved on <strong>Google Drive</strong> in a specified folder.</li>
        <li>Food object detection is performed using a trained model, and the results are stored in a `.txt` file.</li>
        <li>The system reads the result and extracts the class codes of the detected food items.</li>
        <li>The same image is then used for quantity estimation using a different model, which estimates the number of food items based on bounding boxes and reference objects.</li>
        <li>The quantity and nutritional content of the detected food are calculated and sent as a <strong>JSON response</strong> to the client.</li>
      </ul>
    </td>
  </tr>
</table>

#### 3. Recipe Recommendation
<table>
  <tr>
    <td>
      <p align="center">
        <img src="https://github.com/user-attachments/assets/ccab78fe-5586-4add-bdba-ab953f8e12a2" width="80%">
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <ul>
        <li>The recommendation system provides two recipes based on the user's information, such as age, gender, and dietary preferences.</li>
        <li>First, food data is filtered based on a 7:3 ratio between ingredients and tags.</li>
        <li>Nutritional components like carbohydrates, proteins, and fats are converted into vectors, and cosine similarity with the user's vector is used to generate the first recommendation.</li>
        <li>The second recommendation is based on the first recommendation and other users' consumption patterns, using a <strong>NGCF-based model</strong> in the RecBole framework to predict similar items.</li>
      </ul>
    </td>
  </tr>
</table>

<br>

## Application
<!--### 🎞️ [Video](https://youtu.be/neTSmxHLIRQ?si=FmVLHrGp9E3OCn7v) 🎞️-->
|Landing|SignUp 1|SignUp 2|SignUp 3|
|:------:|:-----:|:-----:|:-----:|
|<img src="https://github.com/user-attachments/assets/48682f1f-c726-43a1-80a4-727748d60577" width="250">|<img src="https://github.com/user-attachments/assets/16e3303d-2cec-4c1b-b794-656f8a1b5578" width="250">|<img src="https://github.com/user-attachments/assets/9e0e6784-cf2b-4586-b8ae-77d3c4ba0f41" width="250">|<img src="https://github.com/user-attachments/assets/5ac7363e-1f6a-41f8-8b55-11502fdf412b" width="250">|

|SignUp 4|Login|Dashboard|Meal Recording|
|:------:|:-----:|:-----:|:-----:|
|<img src="https://github.com/user-attachments/assets/fbc3cb3a-bd28-4e00-b210-9f167f3fa502" width="250">|<img src="https://github.com/user-attachments/assets/c37075bf-f5a2-482d-bfb0-c32980c8ee49" width="250">|<img src="https://github.com/user-attachments/assets/11b3ced2-d614-4b18-b8d1-ceb230b523e7" width="250">|<img src="https://github.com/user-attachments/assets/7860efae-bb5c-4b88-ac0e-aa53bb0c6f20" width="250">|

|Statistics|Search Ingredients|Recipe Recommendation|Profile|
|:------:|:-----:|:-----:|:-----:|
|<img src="https://github.com/user-attachments/assets/ad8688a9-b591-412d-98df-6fea7150e100" width="250">|<img src="https://github.com/user-attachments/assets/52e7f130-a478-485d-b769-051a5f5796d4" width="250">|<img src="https://github.com/user-attachments/assets/21533f2b-8441-4ea3-9970-44581552d9d6" width="250">|<img src="https://github.com/user-attachments/assets/a07f3039-0a0b-4a19-8248-c28d189e1594" width="250">

<br>

## Members
<div>
  <table align="center">
      <tr>
         <td align="center">
          <a href="https://github.com/alsrudursla">                 
              <img src="https://avatars.githubusercontent.com/alsrudursla" width="150" />            
          </a>
          </td>
          <td align="center">
              <a href="https://github.com/great-whiteshark">                 
                  <img src="https://avatars.githubusercontent.com/great-whiteshark" width="150" />            
              </a>
          </td>
          <td align="center">
              <a href="https://github.com/glyserin">                 
                  <img src="https://avatars.githubusercontent.com/glyserin" width="150" />            
              </a>
          </td>
      </tr>
      <tr>
          <td align="center"><a href="https://github.com/alsrudursla">Minkyung Lee</td>
          <td align="center"><a href="https://github.com/great-whiteshark">Sangah Park</td>
          <td align="center"><a href="https://github.com/glyserin">Serin Cheong</td>
      </tr>
      <tr>
          <td align="center"><a href="https://github.com/Bab-Al/Babal-Server">Backend</a> & <a href="https://colab.research.google.com/drive/1iPOW8daDEVpywfpSz49TdZ_2xl2DIa-c?ouid=0&usp=chrome_ntp">AI (Recipe Recommendation)</a></td>
          <td align="center">AI (Food Object Detection & Nutrient Estimation)</td>
          <td align="center"><a href="https://github.com/Bab-Al/Babal-iOS">Frontend</a> & Embedded System</td>
      </tr>
  </table>
</div>

<br>

## History ... 🗝️
- <a href="https://docs.google.com/presentation/d/1QrXeJSxBtcstQ_Zlqwcslb58-KhQvGwz/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">Project Proposal
- <a href="https://docs.google.com/presentation/d/1JiIgi8jT8OxlzkW1yJh-92o-bsgXVcgb/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">1st Semester Mid-term
- <a href="https://docs.google.com/presentation/d/14JxHUYh8s5p_rD2p4OF90fvD5BDoZupl/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">1st Semester Final
- <a href="https://docs.google.com/presentation/d/1JzbhbOjaKnPiNo5ilgzPBzcCjH2JMH8k/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">2nd Semester Mid-term
- <a href="https://docs.google.com/presentation/d/1AUCGKxoDh1jkbA120qPAnuFhUc49Ij1t/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">2nd Semeter Final
- <a href="https://docs.google.com/presentation/d/12fUdrlWIgzY9HeWGDnD6bRjLianSQhyP/edit?usp=sharing&ouid=100038788088422788715&rtpof=true&sd=true">The Last
