# AI-powered-Stress-Assessment-Tool-for-Biofeedback-Integration-into-the-VMW

# Virtual Meditative Walk (VMW)
The Virtual Meditative Walk (VMW) is an immersive Virtual Reality (VR) system designed to help chronic pain (CP) patients manage pain through Mindfulness-Based Stress Reduction (MBSR) meditation. Unlike traditional pain distraction techniques used in VR for acute pain relief, VMW integrates biofeedback mechanisms to provide real-time adaptive feedback that encourages self-regulation and interoceptive awareness. Chronic pain is a complex, multifaceted condition that often involves emotional, psychological, and physiological dimensions. Traditional pharmacological treatments, including opioids, are limited in long-term efficacy and can carry significant risks. VMW represents an innovative, non-pharmacological approach that uses real-time physiological signals—specifically Electrodermal Activity (EDA) and Heart Rate Variability (HRV)—to dynamically adjust the virtual environment. The system visualizes internal arousal states through environmental changes, such as fog density, allowing users to receive immediate feedback on their stress levels. This immersive feedback loop fosters interoceptive awareness, reinforces relaxation strategies, and enhances self-regulation capabilities over time.

## Environment Design and Biofeedback Integration
VMW places users in a serene virtual forest where they experience a guided meditative walk. The system dynamically adjusts the environment in response to physiological biofeedback data, such as Electrodermal Activity (EDA) and Heart Rate Variability (HRV). These signals, which indicate the user's arousal and stress levels, influence visual and auditory elements in the VR environment. A key feature of this adaptive feedback system is the use of fog density:
*	As stress levels decrease (indicating relaxation), the fog lifts, revealing a clearer landscape.
*	If stress levels rise, the fog thickens, signaling a need to re-engage with relaxation techniques.
This cause-and-effect mechanism reinforces mindfulness training by providing immediate, immersive feedback on the patient’s ability to regulate physiological responses.
## Fostering Attention and Pain Self-Modulation
VMW is not intended as a simple pain distraction tool but as a long-term intervention to train patients in self-modulation of pain. The system aligns with MBSR principles, which emphasize present-moment awareness and acceptance. By visually externalizing internal physiological states, VMW helps patients develop greater control over their stress and pain responses, promoting sustained self-efficacy in pain management.
##User Study and Preliminary Findings
A proof-of-concept study conducted in a clinical setting assessed VMW’s feasibility and effectiveness. Chronic pain patients engaged in 12-minute meditation sessions within VMW, while a control group practiced traditional MBSR meditation without VR. The results indicated:
*	A significant reduction in perceived pain levels among VMW participants compared to the control group.
*	Improved engagement and relaxation responses due to the biofeedback-driven interaction.
*	Increased patient awareness of physiological changes, fostering self-regulation beyond the VR session.
These findings suggest that VMW has strong potential as a non-pharmacological, AI-enhanced intervention for chronic pain management, particularly when paired with biofeedback. Future studies aim to expand on its long-term effects and optimize AI-driven personalization to tailor interventions more precisely to individual users.

## Methodology
This codebase supports a modular development pipeline for building and evaluating machine learning models that detect and classify stress states based on EDA and HRV signals. The included notebooks guide the user through the full process: beginning with feature extraction and signal preprocessing, continuing with exploratory data analysis (EDA) and model training using various machine learning algorithms, and culminating in the real-time integration of the model into the VMW environment. Preprocessing includes denoising, segmentation, and artifact correction of physiological signals using domain-specific techniques such as wavelet decomposition and Butterworth filtering. Feature extraction incorporates a combination of statistical, frequency-domain, and nonlinear measures (e.g., Approximate Entropy, RMSSD, SCR amplitude) to build a rich representation of the user’s stress response. Models such as Random Forest, Gradient Boosting, SVMs, and Neural Networks are evaluated using cross-validation to ensure robustness and generalization.

The final stage of the project focuses on real-time classification and interaction design within the VR environment. A trained model continuously analyzes incoming biometric data, computes a stress index, and modulates the visual properties of the virtual landscape accordingly. For instance, increased stress causes the virtual fog to become denser, signaling users to re-engage with breathing or meditation practices, while a relaxed state lifts the fog, offering a visual cue of progress and reward. This AI-powered feedback loop allows the environment to act not just as a passive space but as an active participant in the therapeutic process—guiding the user toward stress reduction, improving body awareness, and supporting the adoption of long-term mindfulness practices. The project demonstrates how AI and biosignal-driven adaptive systems can transform passive VR experiences into intelligent, therapeutic tools for real-world healthcare applications.


* 1_FeaExt_WESAD.ipynb: This notebook performs feature extraction from the WESAD dataset. It processes raw physiological signals such as EDA, EMG, and respiration to generate meaningful features for stress detection tasks.

* 2_FeaEDA_WESAD.ipynb: This notebook conducts exploratory data analysis (EDA) on the extracted features from the WESAD dataset. It visualizes feature distributions and examines patterns to understand the data structure and stress indicators.

* 3_Train_Models_ML.ipynb: This notebook trains several machine learning models on the extracted features for stress classification. It evaluates model performance using metrics such as accuracy and F1-score, and compares multiple algorithms.

* 4_VMW_Integration.ipynb: This notebook integrates the trained stress detection model into a VMWare-based workflow. It demonstrates model inference in a simulated or real-time environment.



