# リベシティノウハウ図書館分析ツール

## 1. はじめに
このリポジトリはさまざまなプログラムを簡易的にローカルにて実行するために提供されます。

### 前提条件
- Homebrewがインストールされていること
    - 参考：https://brew.sh/ja/
- Pyenvがインストールされていること
    - 参考：https://hitori-sekai.com/python/mac-python-install/

### プロジェクト構成
```
.
├── .venv               # 仮想環境のディレクトリです。
├── .gitignore          # このリポジトリで使用しているファイルの一覧です。
├── .python-version     # このリポジトリで使用しているPythonのバージョンです。
├── main.py             # プログラムのメインファイルです。
├── README.md           # このファイルはこのリポジトリのREADME.mdです。
└── requirements.txt    # このリポジトリで使用しているライブラリの一覧です。
```

## 2. 実行手順
このツールを使用するためには、以下の手順に従ってください。

### 2.0 リポジトリのクローン
1. リポジトリをクローンします。

    ```bash
    git clone https://github.com/yamato-snow/python_testproject_venv.git　<プロジェクト名>
    ```
2. クローンしたリポジトリに移動します。

3. 編集用のブランチを作成します。

    ```bash
    git branch <ブランチ名>
    ```

4. ブランチを切り替えます。

    ```bash
    git checkout <ブランチ名>
    ```

5. プロジェクトを編集します。

6. 編集したプロジェクトをコミットします。

    ```bash
    git commit -m "<コミットメッセージ>"
    ```

7. プロジェクトをプッシュします。

    ```bash
    git push origin <ブランチ名>
    ```

### 2.1. 環境構築
1. 初回の設定（2回目以降の実行時はこの手順は不要です。）

    スクリプトファイルをダウンロードし、任意のディレクトリに保存します。
    Pythonのバージョン（例：3.12.2）をpyenvを使用して指定します。

    ```bash
    pyenv local 3.12.2
    ```

    ※pyenvに指定したバージョンがない場合は、以下のコマンドでインストールします。

    ```bash
    pyenv install 3.12.2
    ```

    Pythonの仮想環境を作成します。
    ```bash
    python -m venv .venv
    ```
2. 仮想環境を有効化します。（2回目以降の実行時はここから開始してください。）

    Windowsコマンドプロンプトでの仮想環境の有効化
    ```bash
    .venv\Scripts\activate.bat
    ```

    macOSでのアクティベーション
    ```bash
    . .venv/bin/activate
    ```

3. 仮想環境内のpipをアップデート（1回目のみ実行してください）

    ```bash
    python -m pip install --upgrade pip
    ```

4. 必要なPythonライブラリのインストール（1回目のみ実行してください）

    ```bash
    python -m pip install -r requirements.txt
    ```

### 2.2. プログラムの実行
1. プログラムを実行するためには、以下のコマンドを入力します。

    ```bash
    python main.py
    ```
2. プログラムが実行されます。

## 4. ライセンス
このスクリプトはMITライセンスに基づいて公開されています。利用規約の詳細については、同梱の`LICENSE`ファイルを参照してください。