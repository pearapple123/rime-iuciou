# wenzhounese-ime
A RIME IME for Wenzhounese. 

It uses the romanisation system from [wugniu.com](https://wugniu.com/search?char=我&table=wenzhou), and uses compounds from 溫州方言詞典（李榮）. In cases where Wugniu did not provide a reading for a character, I either used the reading of characters in the same phonetic series for accuracy, or, failing that, used the reading provided in 方言詞典 and used this to make an approximate reading that uses Wugniu's romanisation.

I would greatly appreciate helpers. If you are interested, please contact me through the ways detailed in my profile's README.

### What I'm currently working on
Adding more compounds using the index in 方言詞典 and Wugniu readings.

### How to install
#### If RIME is already installed
1. Place the `iuciou.dict.yaml` and `iuciou.schema.yaml` files in `C:\Users\[user]\AppData\Roaming\Rime`.
2. Add `- {schema: iuciou}` to `default.custom.yaml` in the same directory, indenting it to be in line with the other schemas.
3. Re-deploy RIME and select an option called "歐語輸入法" in the Ctrl + ` menu.

#### If RIME is not already installed (for Windows)
1. Go to [RIME's website](https:/rime.im) and download Weasel (the one with the Windows logo)
2. Follow the wizard and complete the installation process
3. Check the language tab (the one that says ENG if you're using English etc.) and see if there's an option that looks like this:
  ![RIME option](image.png)
4. Go to `C:\Users\[user]\AppData\Roaming\Rime` and create a file called `default.custom.yaml`. In this, copy this:
```
patch:
  schema_list:
    - {schema: luna_pinyin}
    - {schema: cangjie5}
    - {schema: terra_pinyin}
    - {schema: luna_pinyin_tw}
    - {schema: bopomofo}
    - {schema: bopomofo_express}
    - {schema: cangjie5_express}
    - {schema: stroke}
    - {schema: luna_quanpin}
    - {schema: iuciou}
```
It doesn't have to be exactly like this - remove or add schemas for IMEs you don't need or need respectively. To add schemas, the formula is `- {schema: [schema_id]}` where schema_id can be found in the schema.yaml file of the IME (but is usually the same name as the file name minus the .schema.yaml extension)
5. Re-deploy by clicking on the RIME option (see image above) in the language tab, then right-clicking on the button to the immediate left of the language tab, which will either have an "A" (alphanumeric mode) or "中" (han mode) on it and then clicking on the option in the dropdown list called '重新部署 (R)'
6. If not already in Han mode, click on the button or press Shift to do so.
