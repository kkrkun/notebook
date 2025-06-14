# ベースイメージ（Jupyterの基本イメージ）
FROM jupyter/base-notebook:latest

# rootユーザーに切り替え
USER root

# aptパッケージの更新とsshpassのインストール
RUN apt-get update && \
    apt-get install -y sshpass && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# jupyterユーザーに戻す
USER $NB_UID
