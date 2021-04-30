# Repo for CS 536 Natural Language Processing Final Project

  

## Josh Coward, Ryan Pacheco, Sajia Zafreen

  

## Run

1) Run `pip install -r requriments.txt`

2) Open text_summerization.ipynb using jupyter notebook

3) Run the first cell to import libaries

4) If you want to run and fine tune the BERT model proceed with running the second cell, following instructions in the notebook

****NOTE**** Fine tuning takes a long time on CPU

5) To only look at pre-trained model comparisons go to `Pre trained comp` heading

6) Datasets will be loaded and cleaned. If you wish to use more datasets go to: https://huggingface.co/datasets?filter=task_ids:summarization,languages:en for a list of datasets that can be loaded using the `datasets` library

7) Run the subsequent cells following instructions in the notebook

****NOTE**** Depending on how many articles you wish to run the process can take several days

  

## Example
 At the end of the notebook run `get_summaries` function to see summaries for that article
```
get_summaries(cnn_preds, clean_data_cnn, 1)

Original Article: 
	 CNN The attorney for a suburban New York cardiologist charged in what authorities say was a failed scheme to have another physician hurt or killed is calling the allegations against his client completely unsubstantiated. Appearing Saturday morning on CNN's New Day Randy Zelin defended his client Dr. Anthony Moschetto who faces criminal solicitation conspiracy burglary arson criminal prescription sale and weapons charges in connection to what prosecutors called a plot to take out a rival doctor on Long Island. None of anything in this case has any evidentiary value Zelin told CNN's Christi Paul. It doesn't matter what anyone says he is presumed to be innocent. Moschetto 54 pleaded not guilty to all charges Wednesday. He was released after posting 2 million bond and surrendering his passport. Zelin said that his next move is to get Dr. Moshetto back to work. He's got patients to see. This man while he was in a detention cell the only thing that he cared about were his patients. And amazingly his patients were flooding the office with calls making sure that he was OK Zelin said. Two other men identified as James Chmela 43 and James Kalamaras 41 were named as accomplices according to prosecutors. They pleaded not guilty in Nassau County District Court according to authorities. Both were released on bail. A requests for comment from an attorney representing Chmela was not returned. It's unclear whether Kalamaras has retained an attorney. Police officers allegedly discovered approximately 100 weapons at Moschetto's home including hand grenades high capacity magazines and knives. Many of the weapons were found in a hidden room behind a switch activated bookshelf according to prosecutors. The investigation began back in December when undercover officers began buying heroin and oxycodone pills from Moschetto in what was initially a routine investigation into the sale of prescription drugs officials said. During the course of the undercover operation however Moschetto also sold the officers two semiautomatic assault weapons as well as ammunition prosecutors said. Moschetto allegedly told officers during one buy that he needed dynamite to blow up a building. He later said he no longer needed the dynamite because a friend was setting fire to the building instead. Kalamaras and Chmela are believed to have taken part in the arson according to prosecutors. The fire damaged but did not destroy the office of another cardiologist whose relationship with Dr. Moschetto had soured due to a professional dispute according to the statement from the district attorney's office. Moschetto allegedly gave an informant and undercover detective blank prescriptions and cash for the assault and killing of the fellow cardiologist according to prosecutors. He also requested that the rival's wife be assaulted if she happened to be present authorities said. He was willing to pay 5 000 to have him beaten and put in a hospital for a few months and then he said he would pay 20 000 to have him killed said Assistant District Attorney Anne Donnelly according to CNN affiliate WCBS.

Summaries: 
google/pegasus-cnn_dailymail:
	Dr. Anthony Moschetto's attorney calls the allegations against his client completely unsubstantiated .<n>Moschetto faces criminal solicitation conspiracy burglary arson criminal prescription sale and weapons charges in connection to a plot to take out a rival doctor on Long Island .<n>Police officers allegedly discovered approximately 100 weapons at Moschetto's home including hand grenades high capacity magazines and knives .

t5-base:
	attorney for cardiologist charged in failed scheme to have another doctor hurt or killed . attorney says allegations against his client are completely unsubstantiated . prosecutors say he was willing to pay 5 000 to have him beaten and put in hospital .

sshleifer/distilbart-cnn-12-6:
	 Dr. Anthony Moschetto charged in what authorities say was a failed scheme to have another physician hurt or killed . Police officers allegedly discovered approximately 100 weapons at his home including hand grenades high capacity magazines and knives . Two other men identified as accomplices James Chmela 43 and James Kalamaras 41 have pleaded not guilty in Nassau County District Court .

facebook/bart-large-cnn:
	Dr. Anthony Moschetto faces criminal solicitation conspiracy burglary arson criminal prescription sale and weapons charges. Two other men identified as James Chmela 43 and James Kalamaras 41 were named as accomplices. Police officers allegedly discovered approximately 100 weapons atMoschetto's home.

nsi319/legal-led-base-16384:
	The attorney for a suburban New York cardiologist charged in what authorities say was a failed scheme to have another physician hurt or killed is calling the allegations against his client completely unsubstantiated. Appearing Saturday morning on CNN's New Day, the attorney for a suburban New York cardiologist charged in what authorities say was a failed scheme to have another physician hurt or killed told the network that he was innocent. The attorney also called the allegations against his client completely unsubstantiated. The attorney also called

google/pegasus-newsroom:
	CNN Wanted film director must be eager to shoot footage of golden lassos and invisible jets. CNN confirms that Michelle MacLaren is leaving the upcoming Wonder Woman movie The Hollywood Reporter first broke the story .

google/pegasus-wikihow:
	Get ready for a new director.

ml6team/mt5-small-german-finetune-mlsum:
	CNN The attorney for a suburban New York cardiologist charged in what authorities say was a failed scheme to have another physician hurtor killed is calling the allegations against his client completely unsubstantiated.
```
