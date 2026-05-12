# BitnetForMultimodal
Use of bitnet for the llm part in a multimodal model. I split it in two different notebooks to keep it more clean and to fit in google colab free version so everyone can test.
- TrainBitnet: Train and save a multimodal model where a llm is using bitnet to generate the texts and clip (frozen) to analize the images.
- InferenceBitnet: The inference part, if you load the training weights, you can see the speed and vram save in the benchmarks.
Time train: Around 3h.
Speed in the llm part is around 2.4 times faster and it goes from 1992mb vram to 90mb vram in saving. Sadly, the final impact for the whole pipeline is almost none as the Clip consume most the time and vram, still i see interesting to show how can bitnet be used in a multimodal selectively havng a real effect in said part, ideal for cases where llm is way bigger.

Conclusion: It is fascinating the idea of bitnet but it was an idea made considering the bottlenecks in transformers llm, in other words, it is not a general solution to implement in every model and its use should be implemented with the correct analysis.

Note: I might update this repository with a different version where i use bitnet in the full pipeline as there are recenly more and more researchs for image using bitnet. Example: https://arxiv.org/abs/2603.09582 
