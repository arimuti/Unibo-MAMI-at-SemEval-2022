# UniBO at SemEval-2022 Task 5: A Multimodal bi-Transformer Approach to the Binary and Fine-grained Identification of Misogyny in Memes

We publish the code for  our submission to SemEval 2022 Task 5 on Multimedia Automatic Misogyny Identification. We address the two tasks: Task A consists of identifying whether a meme is misogynous. If so, Task B attempts to identify its kind among shaming, stereotyping, objectification, and violence.

# Our Approach
We handle the two tasks as five binary classification problems: misogynous vs not, shaming vs not, stereotype vs not, objectification vs not, violence vs not. Then, we adjust the classes for Task B according to the predictions for Task A: if the model for Task A predicts a meme as not misogynous, we ignore the prediction of Task B for that meme.
The code here shows the training and the prediction of class misogynous vs not misogynous; in order to predict the other classes you just need to replace 'misogynous' with the class you want to predict, e.g., 'stereotype', throughout the code. 

Our approach combines a BERT Transformer with CLIP for the textual and visual representations. Both textual and visual encoders are fused in an early-fusion fashion through a Multimodal Bidirectional Transformer with unimodally pretrained components.

# Result
Our official submissions obtain macro-averaged F1=0.727 in Task A (4th position out of 69 participants) and weighted F1=0.710 in Task B (4th position out of 42 participants).

