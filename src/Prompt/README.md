# Simplified Prompt Format for Label Prediction and Label Planning
| Prompt | Component Definition | Example |
|:--|:--|:--|
|Commentary and Transcript Input <br/>(Label Prediction)|Commentary from a commentator regarding the U.S. presidential election.<br/>The transcript is included if available.|This is a commentary made by a commentator regarding the U.S. presidential election: {***commentary***}.<br/> This is the corresponding debate transcript: {***transcript***}. <br/>"***NO***" means no transcript is available.|
|Transcript-Only Input<br/>(Label Planning)|This experiment generates a commentary label based on the U.S. presidential debate transcript. <br/>If the transcript is "***NO***", previous transcripts are merged into a continuous passage for labeling.|This is a transcript of a U.S. presidential election debate: {***transcript***}.<br/>
|Label Definition| 11 labels classify the commentary, including <br/>**Key Summary**, **Fact-Checking**, **Commentator’s Opinion**, etc.<br/> Definitions are provided.|Refer to label definitions: <br/>**Key Summary**, **Fact-Checking**, etc.|
|Prescribed Answer Format| Identify the most likely label based on the transcript and commentary.|Label: **Key Summary**.|
|Example<br/> (Label Prediction)| In this experiment, the model is given a commentary along with a transcript and must predict the correct label for the commentary.|Commentary: {***Insert Commentary***}<br/>Label: {***Corresponding Label***}|
|Example<br/> (Label Planning)| In this experiment, the model receives only a transcript and must generate the appropriate commentary label based on the content of the transcript.|Commentary: {***Insert Commentary***}<br/>Transcripts: {***Insert Transcripts***}<br/>Label: {***Corresponding Label***}
