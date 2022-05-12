# LVC-VC: End-to-End Zero-Shot Voice Style Transfer using Location-Variable Convolutions

# Abstract

TO-DO

# Audio Demos

## Seen-to-Seen Voice Conversion

<div class="row" width="auto">
    <div class="col-12">
        <table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
          <thead>
            <tr>
              <th style="width: 15%">Source Speaker</th>
              <th style="width: 15%">Target Speaker</th>
              <th style="width: 40%">Converted Output</th>
              <th style="width: 40%">         </th>
            </tr>
          </thead>
            
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p241 (Male)</p>
                <audio id="player" controls >
                    <source src="audio/vctk_orig/p241_302.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p334 (Male)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AdaIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/adain/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AGAIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/again/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls>
                    <source src="audio/autovc/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls>
                    <source src="audio/autovc_f0/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls>
                    <source src="audio/blow/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls>
                    <source src="audio/nvcnet/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls>
                    <source src="audio/lvc_vc/s2s/p241_302_p334_396.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

              
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p241 (Male)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p241_237.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p228 (Female)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AdaIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/adain/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AGAIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/again/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls>
                    <source src="audio/autovc/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls>
                    <source src="audio/autovc_f0/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls>
                    <source src="audio/blow/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls>
                    <source src="audio/nvcnet/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls>
                    <source src="audio/lvc_vc/s2s/p241_237_p228_313.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>

<div class="row">
    <div class="col-12 ml-auto">
        <table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px">
          <thead>
            <tr>
              <th style="width: 15%">Source Speaker</th>
              <th style="width: 15%">Target Speaker</th>
              <th style="width: 40%">Converted Output</th>
              <th style="width: 40%">         </th>
            </tr>
          </thead>
            
          <tbody>
            <tr>
              <td rowspan="4" style="vertical-align: top;"><p>p247 (Male)</p>
                <audio id="player" controls >
                    <source src="audio/vctk_orig/p247_311.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="4" style="vertical-align: top;"><p>p245 (Male)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AdaIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/adain/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AGAIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/again/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls>
                    <source src="audio/autovc/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls>
                    <source src="audio/autovc_f0/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls>
                    <source src="audio/blow/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls>
                    <source src="audio/nvcnet/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls>
                    <source src="audio/lvc_vc/s2s/p247_311_p245_143.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>

              
            <tr>
              <td rowspan="7" style="vertical-align: top;"><p>p247 (Male)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p241_005.wav" type="audio/wav" />
                </audio>
              </td>
              <td rowspan="7" style="vertical-align: top;"><p>p335 (Female)</p>
                <audio id="player" controls>
                    <source src="audio/vctk_orig/p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AdaIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/adain/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AGAIN-VC</p>
                <audio id="player" controls>
                    <source src="audio/again/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>AutoVC</p>
                <audio id="player" controls>
                    <source src="audio/autovc/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>AutoVC-F0</p>
                <audio id="player" controls>
                    <source src="audio/autovc_f0/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p>Blow</p>
                <audio id="player" controls>
                    <source src="audio/blow/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
              <td><p>NVC-Net</p>
                <audio id="player" controls>
                    <source src="audio/nvcnet/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
            <tr>
              <td><p><b>LVC-VC</b></p>
                <audio id="player" controls>
                    <source src="audio/lvc_vc/s2s/p241_005_p335_355.wav" type="audio/wav" />
                </audio>
              </td>
            </tr>
          </tbody>
        </table>
    </div>
</div>


### Unseen-to-Seen Voice Conversion

### Unseen-to-Unseen Voice Conversion

### Un-targeted Voice Anonymization

<!-- ### Markdown

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
 -->
