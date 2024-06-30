# Improving Kraken’s character segmentation using Energy Minimization

This repository consists of a [project](https://beratkurar.github.io/academic_writings/improving_kraken_character_segmentation_using_energy_minimization.pdf) to improve character segmentation in Kraken using energy minimization framework. In our approach, we assume each character segment in Kraken corresponds to one and only one character, but each character might consist of several connected components. 

Using the energy minimization technique, we find a labeling `f` that assigns each component to a label such that the energy function `E(f)` has the minimum value. We use the Euclidean distance between the centroids of the component and the nearest character segment from Kraken as the data cost. For the smoothness cost, we use the cost of assigning neighboring elements to different labels. 

We split a component traversing through several character segments by assigning each pixel in the component to the label of the closest character segment. 

In addition to the implementation of our energy minimization approach, the repository also includes code to read the Alto XML file and visualize it overlapping on the document image. This allows for easier and more accurate analysis of the segmentation results. 

To see the details of the data processing, experimental results, and code implementation, please refer to the [PDF file](https://github.com/beratkurar/visualize_alto_and_refine_kraken_letter_detection/blob/main/character_segmentation_improvement_of_kraken_using_em_IOQS.pdf), which is available in the repository.
