<!DOCTYPE html>
<html>
<head>
    
</head>
<body>
    <h1>Plant Disease Classification using Deep Learning</h1>
    
 <div class="section">
        <p>This project implements various deep learning models to classify plant diseases using the PlantVillage dataset. The system compares the performance of different CNN architectures for automated plant disease detection from leaf images.</p>
    </div>
    
<div class="section">
        <h2>Model Performance</h2>
        <p>The following models were trained and evaluated on the PlantVillage dataset:</p>
        
   <table>
            <tr>
                <th>Model</th>
                <th>Training Accuracy</th>
                <th>Validation Accuracy</th>
                <th>Parameters</th>
            </tr>
            <tr>
                <td class="model-name">9-Layer CNN (Custom)</td>
                <td>97.85%</td>
                <td>93.84%</td>
                <td>3,821,007</td>
            </tr>
            <tr>
                <td class="model-name">MobileNetV2</td>
                <td>96.71%</td>
                <td>92.99%</td>
                <td>2,589,775</td>
            </tr>
            <tr>
                <td class="model-name">VGG16</td>
                <td>92.54%</td>
                <td>90.71%</td>
                <td>14,985,039</td>
            </tr>
            <tr>
                <td class="model-name">ResNet50</td>
                <td>90.89%</td>
                <td>89.57%</td>
                <td>24,644,495</td>
            </tr>
            <tr>
                <td class="model-name">MobileNetV3</td>
                <td>52.22%</td>
                <td>57.01%</td>
                <td>3,246,223</td>
            </tr>
        </table>
            <p><strong>Note:</strong> All models were trained for 20 epochs with a batch size of 16 on 224×224px images.</p>
    </div>
    
<div class="section">
        <h2>Key Observations</h2>
        <ul>
            <li>The custom 9-layer CNN achieved the best validation accuracy (93.84%) despite having fewer parameters than the pretrained models</li>
            <li>MobileNetV2 performed nearly as well as the custom CNN with significantly fewer parameters</li>
            <li>VGG16 and ResNet50 showed good performance but with much higher parameter counts</li>
            <li>MobileNetV3 underperformed compared to other architectures in this implementation</li>
            <li>All models except MobileNetV3 achieved validation accuracy above 89%</li>
        </ul>
    </div>
    
  <div class="section">
        <h2>Training Details</h2>
        <ul>
            <li><strong>Dataset:</strong> 16,516 training images, 4,122 validation images (20% split)</li>
            <li><strong>Image Size:</strong> 224×224 pixels</li>
            <li><strong>Augmentation:</strong> Rescaling (1./255)</li>
            <li><strong>Optimizer:</strong> Adam</li>
            <li><strong>Loss Function:</strong> Categorical Crossentropy</li>
            <li><strong>Epochs:</strong> 20</li>
            <li><strong>Batch Size:</strong> 16</li>
        </ul>
    </div>
    
 <div class="section">
        <h2>Visualizations</h2>
        <p>The notebook generates comprehensive visualizations for each model including:</p>
        <ul>
            <li>Training vs Validation accuracy plots</li>
            <li>Training vs Validation loss plots</li>
            <li>Confusion matrices</li>
            <li>Model architecture summaries</li>
        </ul>
        <p><strong>View complete model results:</strong> <a href="https://drive.google.com/drive/folders/1XrPfZo8NKgf6ebo7yAnF0jVtWxb1Yfd9?usp=drive_link" target="_blank">Google Drive Folder</a></p>
    </div>
    
 <div class="section">
        <h2>How to Run</h2>
        <div class="highlight">
            <ol>
                <li>Upload the notebook to Google Colab</li>
                <li>Select GPU runtime (Runtime → Change runtime type → GPU)</li>
                <li>Run all cells sequentially</li>
                <li>Models will automatically train and generate evaluation metrics</li>
            </ol>
            <p>Required dependencies:</p>
            <code>!pip install -q kaggle tensorflow gradio</code>
        </div>
    </div>
    
 <div class="section">
        <h2>Future Work</h2>
        <ul>
            <li>Implement more extensive data augmentation</li>
            <li>Experiment with learning rate scheduling</li>
            <li>Add Gradio interface for model deployment</li>
            <li>Extend to more plant disease classes</li>
            <li>Optimize MobileNetV3 performance</li>
        </ul>
    </div>
</body>
</html>
