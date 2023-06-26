### '다중자동분류기'를 텍스트 인식으로 분류 체험해 볼 수 있는 소스 코드입니다. 

#### 인텔 오픈 비노 관련 참고 자료입니다.

1. 텍스트 추출 모델: [링크](https://docs.openvino.ai/2022.3/omz_models_model_horizontal_text_detection_0001.html)
- Inputs<br>
Image, name: image, shape: 1, 3, 704, 704 in the format 1, C, H, W, (C-number of channels, H-image height, W-image width)

- Outputs<br>
The boxes is a blob with the shape 100, 5 in the format N, 5, where N is the number of detected bounding boxes. For each detection, the description has the format: [x_min, y_min, x_max, y_max, conf], where:<br>
(x_min, y_min) - coordinates of the top left bounding box corner<br>
(x_max, y_max) - coordinates of the bottom right bounding box corner<br>
conf - confidence for the predicted class

2. 텍스트 인식 모델: [링크](https://docs.openvino.ai/2022.3/omz_models_model_text_recognition_0014.html)
- Inputs<br>
Image, name: imgs, shape: 1, 1, 32, 128 in the format B, C, H, W, (B-batch size, C-number of channels, H-image height, W-image width) <br>
Note that the source image should be tight aligned crop with detected text converted to grayscale.
- Outputs<br>
The net output is a blob with name logits and the shape 16, 1, 37 in the format W, B, L, where:<br>
W - output sequence length, B - batch size, L - confidence distribution across alphanumeric symbols: #0123456789abcdefghijklmnopqrstuvwxyz, where # - special blank character for CTC decoding algorithm.

3. 참고
- 인텔 OpenVINO Pre-trained 모델에 대해 자세히 알아보고 싶으면 아래 링크를 참고하세요.
https://docs.openvino.ai/2022.3/home.html <br>
https://docs.openvino.ai/2022.3/openvino_docs_install_guides_install_dev_tools.html#install-dev-tools

- 인텔 OpenVINO Pre-trained 모델 파일 다운로드 하고 싶으면 아래 링크를 참고하세요.
https://storage.openvinotoolkit.org/repositories/open_model_zoo/2022.3/models_bin/1/

- 인텔 OpenVINO Model Zoo 다양한 Pre-trained 모델을 확인할 수 있습니다.
https://github.com/openvinotoolkit/open_model_zoo/tree/master/models
