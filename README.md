### **Golf Ball Detection and Trajectory Tracking with DETR** 🏌️‍♂️🎯  

This repository provides a **deep-learning-powered pipeline** for **golf ball detection and trajectory tracking** in videos using **DETR (DEtection TRansformer)**. The system is optimized for **real-time processing**, making it highly suitable for **sports analytics**, **automated tracking systems**, and **AI-driven video analysis**.  

---

## **🔹 Features & Technical Highlights**  

✅ **DETR-based Object Detection** – Utilizes **DETR (facebook/detr-resnet-50)** for **bounding box detection** of golf balls in videos.  
✅ **End-to-End Pipeline** – Covers **video preprocessing, detection, tracking, and annotated output generation**.  
✅ **Advanced Trajectory Tracking** – Implements **momentum-based velocity filtering** to track motion **frame-by-frame**.  
✅ **Occlusion Handling** – Predicts golf ball position when **detections are lost** due to occlusion or motion blur.  
✅ **GPU-Accelerated Inference** – Leverages **PyTorch, TorchVision, and CUDA** for high-speed **real-time** processing.  
✅ **Video Processing with OpenCV** – Reads, processes, and writes **annotated videos** with detected positions and **trajectory paths**.  
✅ **Modular Codebase** – Implements a class-based structure (`GolfBallTracker`) for **scalability and reusability**.  
✅ **Pretrained Model Support** – Easily integrates **custom-trained DETR models** for specialized applications.  

---

## **⚙️ Installation & Dependencies**  

### **1️⃣ Install Required Libraries**  
Ensure you have the required dependencies installed:  

```bash
pip install torch torchvision transformers opencv-python tqdm numpy
```

### **2️⃣ Clone the Repository**  
```bash
git clone https://github.com/your-username/golf-ball-tracking.git
cd golf-ball-tracking
```

### **3️⃣ Run the Detection Pipeline**  
```bash
python track_golf_ball.py --model_path /path/to/model --processor_path /path/to/processor --input_video input.mp4 --output_video output.mp4
```

---

## **📌 Usage Workflow**  

1️⃣ **Load the Pretrained DETR Model & Processor** – Loads the detection model and preprocessor from saved checkpoints.  
2️⃣ **Video Processing** – Reads input frames, converts them to RGB, and prepares them for **DETR inference**.  
3️⃣ **Object Detection** – Runs the **DETR model** to detect golf balls and extract **bounding box coordinates**.  
4️⃣ **Trajectory Tracking** – Smooths motion using **velocity-based estimation** and **momentum filtering**.  
5️⃣ **Handling Missing Detections** – If no detection is found, the system **predicts the next position** based on previous movement.  
6️⃣ **Visualizing the Trajectory** – Draws **bounding boxes and trajectory paths** on the output video.  
7️⃣ **Saving the Processed Video** – Writes the annotated frames into an **output file** for analysis.  

---

## **🚀 Applications & Use Cases**  

✔️ **Sports Analytics** – Helps in **game analysis** by tracking **ball movement and speed**.  
✔️ **AI-Powered Training Systems** – Assists golfers in improving their swings with **trajectory insights**.  
✔️ **Automated Object Tracking** – Extends to other applications, including **tennis, baseball, and soccer ball tracking**.  
✔️ **Augmented Reality (AR) & Broadcast Systems** – Enhances sports broadcasting with **real-time tracking overlays**.  

---

## **🛠 Future Improvements**  

🔹 **Multi-Object Tracking** – Extend tracking to detect **multiple balls or players** in a video.  
🔹 **3D Trajectory Estimation** – Implement **depth estimation** for more **accurate trajectory prediction**.  
🔹 **Custom Training** – Train DETR with **larger datasets** for enhanced **detection accuracy**.  
🔹 **Mobile Deployment** – Optimize the model for **edge devices and mobile applications**.  

---

## **📜 License**  
This project is open-source and available under the **MIT License**.  

🎯 **Contributions & feedback are welcome!** Feel free to fork, enhance, and share your improvements. 🚀🏌️‍♂️
