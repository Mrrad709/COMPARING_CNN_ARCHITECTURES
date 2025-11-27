🏠 House Price Prediction - CNN Architecture Comparison  
📖 Overview  

This project conducts an extensive evaluation of 21 convolutional neural network architectures for predicting property prices using Zimbabwe real estate data. The implementation features a sophisticated multi-modal approach that combines visual features from property images with structured property metadata.

🎯 Research Question  
Which CNN architecture provides the most effective visual feature extraction when integrated with tabular property data for accurate price prediction?

🏗️ Model Architectures Tested  
🔬 Modern & Efficient  
EfficientNet ⭐ - MobileNet-v2 ⭐ - ResNet ⭐

DenseNet - Xception

🧠 Inception Family
Inception-V3 - GoogleNet

Inception-ResNet-v2 - Inception-V4

🏛️ Classic Foundations
VGG - AlexNet - NIN - ZFNet

🔬 Research Variants
Squeeze-and-Excitation - Residual-Attention - WideResNet

Competitive-SE - HRNetV2 - FractalNet

Highway Networks - CapsuleNet

📊 **Dataset & Features**  
Property Data (1,610 listings)
Data Type	Features	Processing
Structured	Price, bedrooms, bathrooms, area, location	StandardScaler, LabelEncoder
Visual	Property photographs	224×224 resolution, ImageNet normalization
Target	Price (USD)	StandardScaler normalized
🔧 Intelligent Data Handling
Missing image imputation with black placeholders
Geo-encoding for location data
Feature engineering for property attributes

⚙️ **Technical Implementation**
Multi-Modal Architecture
python
PropertyValuationNetwork(
    base_architecture,    # CNN backbone (21 variants)
    feature_count=5,      # Tabular features
    dropout_rate=0.5,     # Regularization
    architecture_variant  # Model-specific adaptations
)
Training Configuration
Loss Function: Composite (50% L1 + 50% MSE)
Optimizer: AdamW (lr=0.0021, weight_decay=1e-4)
Scheduler: ReduceLROnPlateau (factor=0.7, patience=6)
Early Stopping: Patience of 10 epochs
Batch Size: 16 (GPU memory optimized)

📈 **Performance Insights**
🏆 Top Performers
EfficientNet - Best balance of accuracy and efficiency
MobileNet-v2 - Fast training with competitive results
ResNet - Strong feature extraction capabilities  

⚡ **Computational Findings**
Training Time: Varied from ~20 minutes to several hours per architecture
Model Size: Ranged from 8M to 30M parameters
Convergence: Most models showed similar loss patterns despite architectural differences

🎯 **Key Observations**
Multi-modal fusion consistently outperformed single-modality approaches
Lighter architectures (MobileNet) offered best training efficiency
Data quality and price variance were significant challenges
