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

<table class="table table-responsive align-content-center" style="background-color: whitesmoke; border-radius: 20px; width: 100%">
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
