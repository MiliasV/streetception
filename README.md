# Streetception
### How safe or attractive do different people perceive streets to be and why?

#### In this repository we share the code and data we collected and analysed for the paper "Is it safe to be attractive? Disentangling the influence of streetscape features on the perceived safety and attractiveness of city streets".

The data contain  ratings of perceived safety and attractiveness (using a 5-point Likert scale) coming from 403 participants who were asked to virtually navigate city streets in Frankfurt, Germany, through a sequence of street-level images. Moreover it contains their explanations of the ratings (in their own words).

In total we have collected data for 753 locations. 
In particular:
* 7989 rating pairs of perceived safety and attractiveness
* 19114 keywords used to explain the safety ratings
* 18232 keywords used to explain the attractiveness ratings


## Data
A DOI to the data can be found here: https://doi.org/10.5281/zenodo.7712811

### Structure of the data

### [data_per_location.csv]
| geometry_text       | path_id | image_point_id | order_id | {safety,attractiveness}_{avg,stddev,difff}| {safety,attractiveness}_reason  | {male, female, age_19_39_safety, age_40_59_safety, age_60_plus_safety}_{avg, count}
| :---        |    :----   |          :--- |            :--- |    :--- |    :--- |  :--- | 
| EPSG:4326   | id of the path this location belongs to | id of the image  | order of location in the path | Average, Stddev, and difference of the safety and attractiveness ratings collected for this location (number) | Reasons to explain the safety and attractiveness ratings the participants provided (text input)| Number and average ratings of safety and attractiveness the participants provided per gender and age group| 

### [text_attr_peruser.txt, text_unattr_peruser.txt, text_safe_peruser.txt, text_unsafe_peruser.txt]
All reasons participants provided to explain the ratings of locations with a rating of safety or (attractiveness):
* rating <= 2.5 (text_unattr_peruser.txt, text_unsafe_peruser.txt)
* rating >=3.5 (text_attr_peruser.txt, text_safe_peruser.txt)


## Example
<p align="center">
    <img src="https://github.com/MiliasV/streetception/blob/main/img_gh/path_compl.png" width="70%">
</p>

## Notebooks
Under the folder "notebook" you can find two notebooks
* analysis_experimentation.ipynb: contains code for the analysis of the influence/relation of safety and attractiveness using the participation rating
* word_analysis.ipynb: contains code for the analysis of the text-based input collected from the participants
