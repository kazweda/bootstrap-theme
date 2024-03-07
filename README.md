# bootstrap-theme

こちらの記事を参考にカスタマイズしてみました。
- [Bootstrap5をSassでカスタマイズする方法](https://oopsoop.com/how-to-customize-bootstrap-5-with-sass/)

## 環境構築
### anyenv
node環境(nodenv)はanyenvを使って導入しています。

- [anyenv](https://github.com/anyenv/anyenv)
- [anyenvの環境構築](https://qiita.com/282Haniwa/items/71a48a10952413416d18)

### anyenv, nodenvのインストール
```
git clone https://github.com/anyenv/anyenv ~/.anyenv
```

- PATHを設定(zsh)
```
echo 'export PATH="$HOME/.anyenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(anyenv init -)"' >> ~/.zshrc
```

- shellを再起動して動作確認
```
exec $SHELL -l
anyenv --version
anyenv install --init
```

- nodenvをインストール
```
anyenv install --list
anyenv install nodenv
exec $SHELL -l
```

### bootstrap
```
npm install bootstrap
```
### sass
- [sass install](https://sass-lang.com/install/)

```
npm install --save-dev sass
nodenv rehash
sass --version
```
## scssのコンパイル
sassコマンドでscssファイルをコンパイルしてcssファイルを生成します。
```
cd css
sass -s compressed custom.scss bootstrap.min.css
```