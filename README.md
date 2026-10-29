# postcards-from-my-jungle
# A 250-350 word description of the work in the README.md file, explaining:
## your strategies for training the models

originally i had atempted to manually code the model/training using the notebook referenced in class. I had great difficulty with what it produced, one session of training lasting past 4 hours before I stopped it since it had only completed one epoch. It was at this point that I realized the data subset trained the machine on was far too large and i opted to reduce it and the amount of steps (initially 10 000 steps). I had also recognized at this point that I was in fact training my model using a CPU and not a GPU, which contributed to the incredibly long training duration. 

Once I had reduced both the steps and epochs to 50, I ran the training code which completed in about 25 minutes. I was ultimately unsatisfied with the lack of clarity in the images so I reviewed my code and settings.

Once I realized that the notebook linked in the instructions was seperate from that which was used in class, and that it contained all the necessary code, I opted to use that. At this point I selected the following settings:
- IMAGE_SIZE    = 64      # 64×64 pixels (32 trains faster, 128 is much slower)
- BATCH_SIZE    = 32      # images per training step
- TRAIN_STEPS   = 5000    # total training steps (more = better, slower)

Knowing now to select the GPU for runtime use, I did so. I also decided to halve my initial step count. Since I knew it was not the primary cause of my initial slow progress, I didn't reduce it further but I also recognized that having 10 000 steps was absurdly high. I aimed for a middle ground with my other settings and this time the trainning took 2.5 hours to complete. (I understand this was still quite long but I did not want to further reduce my steps at the expense of my images)

I know that the quality of my generated animals could be improved should I increase the amount of data in my training subset (though this was not entirely feasable concidering the amount of processing power I had at my disposal). I also recognize that the data I used was not entirely selective, in that the subject was not always centered and posed the same way in each image. Notably each image also had a large degree in variance for backgrounds, something that could easily confuse the training. If I wanted to improve this I could have instead sought out images that have blank backgrounds or edited the "unimportant" background details out. Additionally I would have liked if the images were 128 pixels instead of 64, this would have improved the clarity of my input images and inturn, provide greater context to the model. (Though this would have taken and extremily long time to train)

I used the codex AI extension to help debug and generate html and css code for my website. I stuck to using the similarly unpaid version in my google colab, relying on the free (but slower) T4 GPU.


To generate sounds and text for each animal, i took inspiration from the most closely related dataset image. What ever the generated "animal" closest resembles is the starting point for the sound it generates. My goal in doing this is the create an uncanny sensation in the viewer, some animals could make the sounds associated with the image, others look nothing like animals. 
## how you generated your fictional beasts' images, sounds, and language
## how the quality of the images and sounds could be improved.
## If you used any AI assistance or agent, which tool did you use? Was it the free or the paid version?
