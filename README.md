# Streetception
### How safe or attractive do different people perceive streets to be and why?

#### In this repository we share the code and data we collected and analysed for the paper "Is it safe to be attractive? Disentangling the influence of streetscape features on the perceived safety and attractiveness of city streets".


City streets that feel safe and attractive motivate active travel behaviour and promote people’s well-being. However, determining what makes a street safe and attrac- tive is a challenging task because subjective qualities of the streetscape are difficult to quantify. Existing evidence typically focuses on how different street features influ- ence perceived safety or attractiveness, but little is known about what influences both. To fill this knowledge gap, we developed a crowdsourcing tool and conducted a study with 403 participants, who were asked to virtually navi- gate city streets in Frankfurt, Germany, through a sequence of street-level images, rate locations based on perceived safety and attractiveness, and explain their ratings. Our re- sults contribute new insights regarding the key similari- ties and differences between the factors influencing per- ceived safety and attractiveness. We show that the presence of human activity is strongly related to perceived safety, whereas attractiveness is influenced primarily by aesthetic qualities, as well as the number and type of amenities along a street. Moreover, we demonstrate that the presence of construction sites and underpasses has a disproportion- ately negative impact on perceived safety and attractive- ness, outweighing the influence of any other features. We use the results to make evidence-informed recommenda- tions for designing safer and more attractive streets that encourage active travel modes and promote well-being.


## Data
### Structure of the data
#### data_per_location.csv
| geometry_text       | path_id | image_point_id | order_id | {safety,attractiveness}_{avg,stddev,difff}| {safety,attractiveness}_reason  | {male, female, age_19_39_safety, age_40_59_safety, age_60_plus_safety}_{avg, count}
| :---        |    :----   |          :--- |            :--- |    :--- |    :--- |  :--- | 
| EPSG:4326   | id of the path this location belongs to | id of the image  | order of location in the path | Average, Stddev, and difference of the safety and attractiveness ratings collected for this location (number) | Reasons to explain the safety and attrractiveness ratings the participants provided (text input)| Number and average ratings of safety and attractiveness the participants provided per gender and age group| 


## Example
<p align="center">
    <img src="https://github.com/MiliasV/streetception/blob/main/img_gh/path_compl.png" width="70%">
</p>

## Notebooks
Under the folder "notebook" you can find two notebooks
* analysis_experimentation.ipynb: contains code for the analysis of the influence/relation of safety and attractiveness using the participation rating
* word_analysis.ipynb: contains code for the analysis of the text-based input collected from the participants
