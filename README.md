# Detector de gestos da mão

Reconhece o gesto de "joinha" pela webcam e responde na tela com **CURTI** ou
**NÃO CURTI**, conforme o polegar estiver apontado para cima ou para baixo.

## Como funciona

1. O OpenCV captura a imagem da webcam quadro a quadro
2. O MediaPipe Hands localiza os 21 pontos de referência da mão
3. O programa verifica, dedo a dedo, se as quatro pontas (indicador, médio, anelar e
   mínimo) estão dobradas em direção à palma
4. Com todos os dedos dobrados, a altura do polegar decide a resposta: acima da junta é
   CURTI, abaixo é NÃO CURTI
5. O resultado aparece escrito na imagem, em verde ou vermelho

As pontas dos dedos são marcadas com círculos: verde quando o dedo está dobrado,
vermelho quando está estendido.

## Tecnologias

- Python
- OpenCV — captura e exibição do vídeo
- MediaPipe — detecção da mão e dos pontos de referência

## Como executar

```bash
pip install opencv-python mediapipe
python PRO-C121/sign_language.py
```

Precisa de uma webcam conectada.
