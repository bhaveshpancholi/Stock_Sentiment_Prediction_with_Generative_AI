# Stock_Sentiment_Prediction_with_Generative_AI
Predicting sentiment of the stocks based on the latest corporate announcements by a Generative AI approach.

The following steps were taken:
1. Collected the raw data of the company announcements from stock exchange websites including BSE and NSE.
2. Every listed company submits the latest information and updates to the stock exchange in the form of a pdf document. Used PyPDF2 package to extract the contents of the pdf document.
3. Preparing supervised dataset:
- Used Open AI model(text-davinci-002) to make predictions for the extracted pdf data.
- Extracted pdf texts were used as input and OpenAI predictions were used as a target.
- Prepared the dataset for training, validation, and testing. 
4. Used open-source Large Language Models (Llama-7b, Dolly-3b, GPT2-large) to finetune the model using State-of-the-art Parameter-Efficient Fine-Tuning (PEFT) LoRA method.
5. Performed different experiments by changing various combinations of hyperparameters.
6. After completion of every experiment, generated Blue, Rougue1, RougueL, and Semantic Similarity scores on the test dataset. The scores were compared with other experiment's scores.

Outcome:
1. Llama-7b model was performing better than Dolly-3b and GPT2-Large models.
2. While comparing with ChatGPT result, the best Llama finetune model yields the following scores.
- In terms of precision-based metrics, Bleu Score produces 54%.
- In terms of recall metric, Rougue1, and RougueL Scores produce 64% and 49% respectively.
- In terms of cosine similarity, Similarity Score produces 90%.
