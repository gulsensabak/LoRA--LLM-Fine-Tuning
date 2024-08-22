# LoRA (Low Rank Adaption)

LoRA allowing you to finetune only a small number of extra weights in the model while freezing most of the parameters of the pre trained network.

Key idea here: we are not actually training the original weights. We are adding some extra weights. We are going to fine tune those.

One of the main advantages of LoRA is: We have got original weights so this tends to help with stopping catastrophic forgetting. (Catastrophic forgetting: Models tend to forget what they were originally trained on when you do a fine tuning. If you do fine tuning too much, you may end up with catastrophic forgetting.)


The aim is not creating copies of foundation model. (copies that are specialized on different tasks) We get this from regular fine tuning process.

In LoRA, we are talking about adapters whihc are small neural networks that they can plug in into different layers of the foundation models.

In summary, there exist a foundation model plus small adapters that are going to make that foundation model act differently.

We can load these adapters together with a model to dynamically transform its capabilities.
