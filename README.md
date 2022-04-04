# Live camera view in Jupyter Notebook

Gilbert François Duivesteijn

## Abstract

Jupyter Notebook and JupyterLab are great tools for research and documentation. The ability to combine running code with plots and latex formulas is amazing. However, what is not so trivial is to have a live camera or video feed inside a Jupyter Notebook. Moreover, with cloud computing (e.g. Google Colab, AWS Sagemaker, your own remote server, etc), the Jupyter Notebook server is not always running on the computer where the camera is connected. E.g. when running a notebook in the cloud and want to use the local webcam from the computer or iPad, that is not trivial. 

This repository aims to have most use cases covered with the most simple example that you can tweak to your own needs.



## Jupyter with cv2.VideoCapture and ipywidgets

- Jupyter server and the camera are on the same computer (local/local or remote/remote).
- The camera is an e.g. IP camera with RTSP stream.
- Jupyter server and the video source are on the same computer.
- The camera is directly connected to a remote Jupyter server via USB or build-in.




## Jupyter with ipyWebRTC and ipywidgets

- The camera is connected to the local computer and the Jupyter server is running remotely (e.g. Google Colab, AWS Sagemaker, your own remote server, etc).

This notebook shows how to grab and send the frames from the local webcam to the remote server, process them and show them "live" in the Jupyter notebook.



|  Jupyter Notebook Server  |  Camera       | Method to use...             |
|---                        |---            |---                           |
| local                     | local         | cv.VideoCapture (or iPyWebRTC) |
| local                     | remote (RTSP) | cv.VideoCapture              |
| remote                    | local         | iPyWebRTC                    |
| remote                    | remote        | cv.VideoCapture              |



