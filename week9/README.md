For this project, I fine tuned Llama 3 8B using QLoRA. The goal was to create a model that generates video game scene cards. Each scene card includes a scene title, narration, image prompt, negative prompt, audio cue and player choices.

The model was trained using 230 examples, with 207 used for training and 23 used for validation. The dataset included 24 settings, 8 moods, 5 times of day and 4 types of constraints.

Project Links

Hugging Face Model:
https://huggingface.co/giashere0/llama3-8b-game-scene-qlora

Gradio Demo:

https://7f5264c20b6af7cf33.gradio.live

Key Metrics

Final training loss: 0.0044
Final validation loss: 0.0121
Training time: 12.5 minutes on Google Colab
Training loss decreased from 1.892 to 0.004.
Automatic format score: Improved from 0.0 to 1.0.

Model Performance

The fine tuned model performed better than the original model. The average accuracy rating improved from 1.7 to 3.5, the format rating improved from 1.0 to 4.7 and the tone rating improved from 1.8 to 3.8.

These results show that fine tuning helped the model follow instructions and create better video game scene cards.
