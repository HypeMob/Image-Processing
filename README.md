<h1>Project Flow:</h1>

<h2>Dataset Format</h2>
  <img width="907" height="542" alt="Screenshot 2026-09-13 004607" src="https://github.com/user-attachments/assets/67ff89e2-2ae3-4730-8c69-166835af67ec" />
  <h3>Note:</h3>
  <h4>1. Frequency of each separated dataset is the same</h4>
  <h4>2. Class (1) / Positive Demented just means the combination of three classes of the original dataset</h4>
  <h4>3. Each Dataset will be trained using different models</h4>

<h2>Model Architecture</h2>
<img width="860" height="516" alt="Screenshot 2026-09-13 124859" src="https://github.com/user-attachments/assets/5c00be44-38e2-44cf-9c86-648aa491bf55" />
<h3>Note:</h3>
<h4>1. The dataset is separated into two configurations, with each configuration trained using a separate ViT model.</h4>
<h4>2. Model 1 performs 4-class classification.</h4>
<h4>3. Model 2 performs binary (2-class) classification.</h4>

<h2>Model Inference Workflow Pipeline</h2>
<img width="920" height="413" alt="Screenshot 2026-09-13 125514" src="https://github.com/user-attachments/assets/a2670471-ce0f-4ea2-9c34-a11ed1f42911" />
<h3>Flow:</h3>
<h4>1. The MRI scan image (input image) is first processed by Model 2 to determine whether the patient has Alzheimer's disease.</h4>
<h4>2.If the binary classification output is 0, the process stops, indicating that the patient does not have Alzheimer's disease.</h4>
<h4>3. If the binary classification output is 1, the same input image is then processed by Model 1 to determine the severity of the disease.</h4>

<h1>Code File Explanation</h1>
<h2>The Code files are inside the Project folder</h2>
<h3><a href="Project/EDA_Model1.ipynb">1. EDA_Model1 </a></h3>
<h4>This code performs Exploratory Data Analysis (EDA) on Model 1's dataset (4 classes)</h4>
<h4>The EDA includes:</h4>
<ul>
    <li>Bar Chart</li>
    <li>Pie Chart</li>
    <li>Showing Random Images per Class </li>
    <li>Image Dimension Information</li>
</ul>

<h3><a href="Project/EDA_Model2.ipynb">2. EDA_Model2 </a></h3>
<h4>This code performs Exploratory Data Analysis (EDA) on Model 2's dataset (2 classes)</h4>
<h4>The EDA includes:</h4>
<ul>
    <li>Bar Chart</li>
    <li>Pie Chart</li>
    <li>Showing Random Images per Class </li>
    <li>Image Dimension Information</li>
</ul>

<h3><a href="Project/VIT_training1.ipynb">3. VIT_training1 </a></h3>
<h4>This code covers the training and evaluation of Model 1.</h4>
<h4>The code includes:</h4>
<ul>
    <li>Model Configuration</li>
    <li>Data Preprocessing</li>
    <li>Model Training</li>
    <li>Confusion Matrix Evaluation</li>
    <li>Classification Report Evaluation</li>
    <li>Image Testing</li>
</ul>

<h3><a href="Project/VIT_training1.ipynb">4. VIT_training2 </a></h3>
<h4>This code covers the training and evaluation of Model 2.</h4>
<h4>The code includes:</h4>
<ul>
    <li>Model Configuration</li>
    <li>Data Preprocessing</li>
    <li>Model Training</li>
    <li>Confusion Matrix Evaluation</li>
    <li>Classification Report Evaluation</li>
    <li>Image Testing</li>
</ul>

<h1>Code Quick Result</h1>
<h3>VIT 1 Model:</h3>
<ul>
   <li>Accuracy: 0.9975</li>
   <li>Precision: 0.9983</li>
   <li>Recall: 0.9951</li>
   <li>F1-Score: 0.9988</li>
</ul>

<h3>VIT 2 Model:</h3>
<ul>
   <li>Accuracy: 0.8234</li>
   <li>Precision: 0.7798</li>
   <li>Recall: 0.7818</li>
   <li>F1-Score: 0.7805</li>
</ul>

<h1>Contributors</h1>

<h3>This project was collaboratively developed by:</h3>

<ul>
    <li><a href="https://github.com/HypeMob"><strong>Johanes Lie</strong></a></li>
    <li><a href="https://github.com/nekoromancer13"><strong>Devin Jonathan</strong></a></li>
    <li><a href="https://github.com/Hood8833"><strong>Collin Kliveson</strong></a></li>
</ul>



