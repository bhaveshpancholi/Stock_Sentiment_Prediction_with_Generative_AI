# Stock_Sentiment_Prediction_with_Generative_AI
Predicting sentiment of the stocks based on the latest corporate announcements by a Generative AI approach.

The following steps were taken:
1. Collected the raw data of the company announcements from stock exchange websites including BSE and NSE.
2. Every listed company submits the latest information and updates to the stock exchange in the form of a pdf document. Used PyPDF2 package to extract the contents of the pdf document.
3. Preparing supervised dataset   - Used Open AI model(text-davinci-002) to make predictions for the extracted pdf data.
   - pdf extracted texts were used as input and OpenAI predictions were used as a target.
   - Prepared the dataset for training, validation, and testing.
4. Used open-source Large Language Models (Llama-7b, Dolly-3b, GPT2-large) to finetune the model using State-of-the-art Parameter-Efficient Fine-Tuning (PEFT) LoRA method.
5. Performed different experiments by changing various combinations of hyperparameters.
6. After completion of every experiment, generated Blue, Rogue1, RogueL, and Semantic Similarity scores on the test dataset. The scores were compared with other experiment's scores.
