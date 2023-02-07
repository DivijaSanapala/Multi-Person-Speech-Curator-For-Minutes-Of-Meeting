# Multi-Person-Speech-Curator-For-Minutes-Of-Meeting

It is an application that is used to help generate a summary of the recorded meeting using NLP. It is further expanded to identify and label the various speakers involved in the meeting along with the timestamps of each speaker so that the users can re-listen the required part in the audio file.

## Model Workflow
<img width="359" alt="image" src="https://user-images.githubusercontent.com/79396759/217229854-7e21299d-72d9-4787-b5c9-8b87eadf8c34.png">
The architecture above explains the system workflow. The model takes the audio recording of the meeting as input and then the Whisper API encoder-decoder transformer model is used to get the audio to text conversion and then timestamps are generated which consists of the speaker along with the time which is done using agglomerative clustering using Librosa which identifies the speaker labels using the frequency of the voices. After this speaker diarization is used to generate speaker labels along with the text in the transcript.txt file and then this file is passed through text summarization which is done using NLP to generate minutes of meeting. 

## Agglomerative Clustering Flow Diagram
<img width="246" alt="image" src="https://user-images.githubusercontent.com/79396759/217231280-3a1539e4-5d69-4b7b-9002-0763b7501e1c.png">

## Pyannote Architectural Diagram
<img width="467" alt="image" src="https://user-images.githubusercontent.com/79396759/217231523-a93b378c-d98b-493b-9309-5bb9f62fa5bb.png">

## Text Summarization Architecture
<img width="358" alt="image" src="https://user-images.githubusercontent.com/79396759/217231743-94e16eb5-f7e1-4f9a-81a0-51cd3d19f339.png">
