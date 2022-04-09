# R, Rstudioのインストール for macOS

# Rのインストール

1. [R for macOS](https://cran.r-project.org/bin/macosx/)を開き，Rの最新版をダウンロードする．
2. パッケージ `R-バージョン番号.pkg` を開く．指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．
    - バージョン番号はダウンロードのタイミングによって異なるので，各自で読み替えること
3. Rを起動し，Rコンソールが表示されることを確認する．


# RStudioのインストール

1. [rstudio.com](https://www.rstudio.com/products/rstudio/download/)を開き，「All Installers」からmacOS用のディスクイメージをダウンロードする．
2. ディスクイメージ `RStudio-バージョン番号.dmg`を開く（バージョン番号はダウンロードのタイミングによって変わる）
3. RStudioのアイコンをApplicationsのアイコンの上までドラッグして離す．管理者の名前とパスワードを聞かれた場合には入力する．
4. RStudioを起動する．
5. コマンドライン・デベロッパツールをインストールするか聞かれた場合はインストールする．


# RStanのインストール

1. App StoreからXcodeをインストールする．
2. まだコマンドライン・デベロッパツールをインストールしていない場合は，ターミナルを開き，以下のように入力してインストールする．
```
xcode-select --install
```
3. [gfortran for Monterey Intel](https://github.com/fxcoudert/gfortran-for-macOS/releases/download/11.2-monterey-intel/gfortran-Intel-11.2-Monterey.dmg)をダウンロードし、ディスクイメージ `gfortran-Intel-11.2-Monterey.dmg`を開く．パッケージ `gfortran.pkg` を開く。指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．
3. RStudioを起動する．
4. コンソールから以下のように入力する．
   ```
install.packages(c("remotes", "Rcpp", "RcppArmadillo")
```
5. コンソールから以下のように入力する．
```
remotes::install_git("https://github.com/hsbadr/rstan", subdir = "StanHeaders", ref = "develop")
```
6. コンソールから以下のように入力する．
```
remotes::install_git("https://github.com/hsbadr/rstan", subdir = "rstan/rstan", ref = "develop")
```


1. macos-rtools-4.0.0.pkgをダウンロードして開く。
2. 「"macos-rtools-4.0.0.pkg"が悪質なソフトウェアかどうかをAppleでは確認できないため、このソフトウェアは開けません。」というダイアログが出たらOKを押して消し、macOSのシステム環境設定を開く。「セキュリティとプライバシー」を選ぶと、「ダウンロードしたアプリケーションの実行許可」の欄に「"macos-rtools-4.0.0.pkg"は開発元を確認できないため、使用がブロックされました。」と表示されているので、「このまま開く」を押す。管理者の名前とパスワードを聞かれた場合には入力する．先程と同じダイアログが出るが、今度は「開く」が選択できるので押す。さらに管理者の名前とパスワードを聞かれた場合には入力する．macOS R toolchainインストーラが起動するので、指示に従ってインストーラの操作を進める．「インストール」を押して管理者の名前とパスワードを聞かれた場合には入力する．


https://discourse.mc-stan.org/t/big-sur-installation-instructions-for-r-need-an-update/24351/4