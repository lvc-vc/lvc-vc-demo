## LVC-VC: End-to-End Zero-Shot Voice Style Transfer using Location-Variable Convolutions

## Abstract

TO-DO

## Audio Demos

### Seen-to-Seen Voice Conversion

```html
tr td:last-child {
    width: 1%;
    white-space: nowrap;
}
```
        <section class="page-section bg-primary text-white mb-0" id="many-to-many">
            <div class="container">
                <!-- About Section Heading-->
                <div class="text-center">
                  <h2 class="page-section-heading d-inline-block text-white">MANY-TO-MANY VST</h2>
                                        <p class="pre-wrap lead">All source and target speech are not seen during training</p>
                </div>
                <!-- Icon Divider-->
                <div class="divider-custom divider-light">
                    <div class="divider-custom"></div>
                </div>
                <!-- About Section Content-->
                <div class="row">
                    <div class="col-lg-12 ml-auto">
                        <table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
                          <thead>
                            <tr>
                              <th style="width: 15%">Source Speaker</th>
                              <th style="width: 15%">Target Speaker</th>
                              <th style="width: 40%">Converted</th>
                              <th style="width: 40%">         </th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p226 (Male)</p>
                                <audio id="player" controls >
                                    <source src="audio/seen/source/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="4" style="vertical-align: top;"><p>p256 (Male)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/target/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/startganvc/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/againvc/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau; = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                      
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc32/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16_adv/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                        
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/blow/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                    <source src="audio/seen/voicemixer/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              
                            </tr>

                            <tr>
                                                          <td rowspan="7" style="vertical-align: top;"><p>p226 (Male)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/source/p226_018-to-p256_002.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="7" style="vertical-align: top;"><p>p236 (Female)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/target/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/startganvc/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                         
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/againvc/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
           
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc32/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16_adv/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/blow/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td height="27"><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                    <source src="audio/seen/voicemixer/p226_018-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                          </tbody>
                        </table>
                        
                      <p> </p>  
                        
<table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
                          <thead>
                            <tr>
                              <th style="width: 15%">Source Speaker</th>
                              <th style="width: 15%">Target Speaker</th>
                              <th style="width: 40%">Converted</th>
                              <th style="width: 40%">         </th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p236 (Female)</p>
                                <audio id="player" controls >
                                  <source src="audio/seen/source/p236_021-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="4" style="vertical-align: top;"><p>p259 (Male)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/target/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/startganvc/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/againvc/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                      
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc32/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16_adv/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                        
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/blow/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p236_021-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              
                            </tr>

                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p236 (Female)</p>
                                <audio id="player" controls >
                                    <source src="audio/seen/source/p236_021-to-p236_021.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="7" style="vertical-align: top;"><p>p234 (Female)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/target/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/startganvc/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                         
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/againvc/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
           
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc32/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16_adv/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/blow/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p236_021-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                          </tbody>
                      </table>
                        
                                              <p> </p>  
                        
<table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
                          <thead>
                            <tr>
                              <th style="width: 15%">Source Speaker</th>
                              <th style="width: 15%">Target Speaker</th>
                              <th style="width: 40%">Converted</th>
                              <th style="width: 40%">         </th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p259 (Male)</p>
                                <audio id="player" controls >
                                  <source src="audio/seen/source/p259_004-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="4" style="vertical-align: top;"><p>p270 (Male)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/target/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/startganvc/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/againvc/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                      
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc32/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16_adv/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                        
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/blow/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p259_004-to-p270_024.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              
                            </tr>

                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p259 (Male)</p>
                                <audio id="player" controls >
                                    <source src="audio/seen/source/p259_004-to-p259_004.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="7" style="vertical-align: top;"><p>p240 (Female)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/target/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/startganvc/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                         
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/againvc/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
           
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc32/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/autovc16_adv/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/blow/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p259_004-to-p240_011.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                          </tbody>
                      </table>
                                <p> </p>                           
<table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
                          <thead>
                            <tr>
                              <th style="width: 15%">Source Speaker</th>
                              <th style="width: 15%">Target Speaker</th>
                              <th style="width: 40%">Converted</th>
                              <th style="width: 40%">         </th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p234 (Female)</p>
                                <audio id="player" controls >
                                  <source src="audio/seen/source/p234_007-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="4" style="vertical-align: top;"><p>p226 (Male)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/target/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/startganvc/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/againvc/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                      
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc32/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16_adv/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                        
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/blow/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p234_007-to-p226_018.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              
                            </tr>

                            <tr>
                              <td rowspan="4" style="vertical-align: top;"><p>p234 (Female)</p>
                                <audio id="player" controls >
                                  <source src="audio/seen/source/p234_007-to-p234_007.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td rowspan="7" style="vertical-align: top;"><p>p231 (Female)</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/target/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                              <td><p>StarGAN-VC</p>
                                <audio id="player" controls>
                                    <source src="audio/seen/startganvc/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                         
                              <td><p>AGAIN-VC</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/againvc/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
           
                              <td><p>AutoVC (&tau;  = 32)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc32/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p>AutoVC + <i>L<sub>advsc</sub></i> (&tau;  = 16)</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/autovc16_adv/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                
                              <td><p>Blow</p>
                                <audio id="player" controls>
                                  <source src="audio/seen/blow/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                            <tr>
                              <td><p><b>VoiceMixer (Ours)</b></p>
                                <audio id="player" controls>
                                  <source src="audio/seen/voicemixer/p234_007-to-p231_005.npy.wav" type="audio/wav" />
                                </audio>
                              </td>
                            </tr>
                          </tbody>
                      </table>
                  </div>
                </div>
            </div>
        </section>

### Unseen-to-Seen Voice Conversion

### Unseen-to-Unseen Voice Conversion

### Un-targeted Voice Anonymization

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/lvc-vc/lvc-vc-demo/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
