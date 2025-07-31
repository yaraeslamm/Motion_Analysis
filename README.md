## Motion Analysis using Motion Energy Image (MEI) & Motion History Image (MHI)

---

## Objective

This project analyzes video motion by generating two visual representations:

- **MEI (Motion Energy Image)**: Highlights all regions where motion occurred during the video.
- **MHI (Motion History Image)**: Encodes how recent motion occurred—brighter areas indicate more recent movement.

---

## Methodology

- **Frame Differencing**:  
  Detected motion regions between consecutive frames via thresholding.

- **MEI Computation**:  
  Accumulated binary motion frames to highlight total motion across time.

- **MHI Computation**:  
  Updated a motion history matrix where newer motion appears brighter, and older motion gradually fades.

---

## Output

- `MEI/`: Folder containing intermediate MEI frames  
- `MHI/`: Folder containing intermediate MHI frames  
- `MEI.png`: Final Motion Energy Image  
- `MHI.png`: Final Motion History Image  

---

## ▶How to Run

This project was built in Google Colab.

1. Open the notebook in [Google Colab](https://colab.research.google.com/drive/1lCVuZ0KlK0N2ogeG2UmRsJ6VCwLtwFi1) and save a copy in your Drive 
2. Mount your Google Drive (already included in the code).
3. Upload your `.avi` video to Drive.
4. **Before running, update these paths:**

```bash
base_path = "/content/drive/My Drive"  # Update this to your Drive base folder if different

video_path = os.path.join(base_path, "your_video.avi")  # Replace "your_video.avi" with your file name

mei_folder = os.path.join(base_path, "AVP/MEI")  # You can customize this folder name if needed
mhi_folder = os.path.join(base_path, "AVP/MHI")
```
4. Run the cell. Your final MEI/MHI images and intermediate frames will be saved in the output folders.

##  Requirements

-  Python 3
-  OpenCV
-  NumPy
