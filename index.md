# End-to-End Zero-Shot Voice Conversion with Location-Variable Convolutions

<font size="5"> Wonjune Kang, Mark Hasegawa-Johnson, Deb Roy </font>

## Abstract

Zero-shot voice conversion is becoming an increasingly popular research topic, as it promises the ability to transform speech to sound like any speaker. However, relatively little work has been done on end-to-end methods for this task, which are appealing because they remove the need for a separate vocoder to generate audio from intermediate features. In this work, we propose LVC-VC, an end-to-end zero-shot voice conversion model that uses location-variable convolutions (LVCs) to jointly model the conversion and speech synthesis processes. LVC-VC utilizes carefully designed input features that have disentangled content and speaker information, and it uses a neural vocoder-like architecture that utilizes LVCs to efficiently combine them and perform voice conversion while directly synthesizing time domain audio. Experiments show that our model achieves especially well balanced performance between voice style transfer and speech intelligibility compared to several baselines.

<p></p>

## Audio Demos

This page contains voice conversion samples for LVC-VC applied to audio files from the [VCTK Corpus](https://datashare.ed.ac.uk/handle/10283/3443).
We provide comparisons with six other models: AdaIN-VC, AGAIN-VC, AutoVC, AutoVC-F0, Blow, and NVC-Net.

Additionally, it includes samples from a larger, improved version of the model (not described in the paper), which we call LVC-VC XL. This version of the model uses a larger channel size of 32 (rather than 16) in its LVC layers, utilizes embeddings from [XLSR-53](https://arxiv.org/abs/2006.13979) as content features, and uses information perturbation to extract only linguistic information from them (as done in [NANSY](https://arxiv.org/abs/2110.14513)). It also uses speaker embeddings from [ECAPA-TDNN](https://arxiv.org/abs/2005.07143) rather than [Fast ResNet-34](https://arxiv.org/abs/2003.11982). Please refer to the code for more details.

<!-- Additionally, it contains un-targeted voice anonymization demos for audio files from VCTK and from the [Local Voices Network (LVN)](https://cortico.ai/platform/). Please refer to our paper for the methodology. -->

### Navigation

* [Seen-to-Seen Voice Conversion](#seen-to-seen-voice-conversion)
* [Unseen-to-Seen Voice Conversion](#unseen-to-seen-voice-conversion)
* [Unseen-to-Unseen Voice Conversion](#unseen-to-unseen-voice-conversion)
<!-- * [Un-targeted Voice Anonymization](#un-targeted-voice-anonymization) -->
<!-- * [Un-targeted Voice Anonymization (LVN)](#un-targeted-voice-anonymization-lvn) -->

<p></p>

### Seen-to-Seen Voice Conversion

[Back to top](#audio-demos)

<!-- Source: M1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
          
          <!-- M1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p241 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p241_302.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p334 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- M1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p241 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p241_237.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p228 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: M2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- M2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p247 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p247_311.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p245 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
              
            <!-- M2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p247 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p247_005.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p335 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p247_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p225 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p225_224.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p247 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p247_455.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p225_224_p247_455.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
              
            <!-- F1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p225 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p225_336.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p329 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p329_300.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p225_336_p329_300.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p244 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p244_167.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p254 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p254_109.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p244_167_p254_109.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
              
            <!-- F2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p244 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p244_045.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p314 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p314_265.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/blow/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/s2s/p244_045_p314_265.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

### Unseen-to-Seen Voice Conversion

[Back to top](#audio-demos)

<!-- Source: M1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
          
          <!-- M1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p279 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p279_153.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p315 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p315_009.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p279_153_p315_009.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- M1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p279 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p279_255.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p276 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p276_176.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p279_255_p276_176.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: M2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- M2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p363_194.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p241 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p241_120.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p363_194_p241_120.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- M2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p363_106.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p277 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p277_271.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p363_106_p277_271.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p231 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p231_094.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p374 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p374_332.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p231_094_p374_332.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- F1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p231 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p231_450.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p318 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p318_356.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p231_450_p318_356.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p308 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p308_010.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p256 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p256_079.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p308_010_p256_079.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            
            <!-- F2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p308 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p308_381.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p351 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p351_104.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2s/p308_381_p351_104.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

### Unseen-to-Unseen Voice Conversion

[Back to top](#audio-demos)

<!-- Source: M1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
          
          <!-- M1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p279 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p279_182.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p363_023.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p279_182_p363_023.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- M1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p279 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p279_032.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p240 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p240_184.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p279_032_p240_184.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: M2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- M2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p363_127.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p311 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p311_072.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p363_127_p311_072.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- M2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p363_261.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p312 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p312_322.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p363_261_p312_322.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F1 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F1 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p231 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p231_259.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p326 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p326_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p231_259_p326_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- F1 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p231 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p231_318.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p240 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p240_219.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p231_318_p240_219.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- Source: F2 -->
<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-left" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 25%">Source Speaker</th>
              <th style="width: 25%">Target Speaker</th>
              <th colspan="2">Converted</th>
            </tr>
          </thead>
            
          <!-- F2 to M -->
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p308 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_orig/p308_103.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p311 (Male)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p311_246.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p308_103_p311_246.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

            <!-- F2 to F -->
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p308 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p308_390.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p317 (Female)</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_orig/p317_376.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AdaIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/adain/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
              <td style="width: 25%"><p>AGAIN-VC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/again/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/autovc_f0/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>NVC-Net</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/nvcnet/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC XL</b></p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvc_vc_xl/u2u/p308_390_p317_376.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<p></p>

<!-- ### Un-targeted Voice Anonymization

[Back to top](#audio-demos)

<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-center" style="background-color: whitesmoke; display: table;">
          <thead>
            <tr>
              <th style="width: 50%">Source Speaker</th>
              <th style="width: 50%">Anonymized Output</th>
            </tr>
          </thead>
            
          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p240 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p240_183.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p240_183_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p264 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p264_377.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p264_377_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p308 (Female)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p308_180.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p308_180_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p311 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p311_397.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p311_397_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p326 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p326_194.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p326_194_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>p363 (Male)</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/vctk_anon/p363_106.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/vctk_anon/p363_106_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

        </table>
    </div>
</div>

<p></p> -->

<!-- ### Un-targeted Voice Anonymization (LVN)

[Back to top](#audio-demos)

<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-center" style="background-color: whitesmoke; display: table">
          <thead>
            <tr>
              <th style="width: 50%">Source Speaker</th>
              <th style="width: 50%">Anonymized Output</th>
            </tr>
          </thead>
            
          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 1</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/lvn_anon/Cesar_652_0.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Cesar_652_0_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 2</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/lvn_anon/Christine_909_1.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Christine_909_1_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 3</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/lvn_anon/Dave_666_1.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Dave_666_1_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 4</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/James_795_0.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/James_795_0_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 5</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Miranda_1044_1.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Miranda_1044_1_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

          <tbody>
            <tr>
              <td rowspan="12" style="vertical-align: top;"><p>Speaker 6</p>
                <audio id="player" controls style="width: 100%;" >
                    <source src="audio/lvn_anon/Philomena_773_1.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="12" style="vertical-align: top;"><p>&nbsp;</p>
                <audio id="player" controls style="width: 100%;">
                    <source src="audio/lvn_anon/Philomena_773_1_anon.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>

        </table>
    </div>
</div> -->
