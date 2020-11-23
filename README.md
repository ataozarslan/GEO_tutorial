# GEO_tutorial
This repository contains documentation and code for lecture. 

# 1. derece başlık
## 2. derece başlık 
### 3. derece başlık 

***

- Bu normal fontlu bir cümle.
- _Bu italic fontlu bir cümle._
- *Bu da italic fontlu bir cümle.*

- __Bu kalın fontlu bir cümle_ _
- **Bu da neden kalın fontlu bir cümle olmasın?**


```Python 
    def forward(self, x):
        """Sequentially pass `x` trough model`s encoder, decoder and heads"""
        features = self.encoder(x) # Extract features 

        decoder_output = self.decoder(*features) # Decoder output for segmentation task
        pred = self.segmentation_head(decoder_output) # Feed the decoder output to the segmentation head

        reconstruct_decoder_output = self.skipless_decoder(*features) # Decoder output for reconstruction task
        reconst_mask = self.reconstruct_segmentation_head(reconstruct_decoder_output) # Feed the decoder output to the reconstruction head

        return pred,reconst_mask
```
## If you find our work beneficial, consider citing our paper! 

Dataset used in this work is from SpaceNet6 challange. See the arXiv paper here: ["SpaceNet 6: Multi-Sensor All Weather Mapping Dataset"](https://arxiv.org/abs/2004.06500)




