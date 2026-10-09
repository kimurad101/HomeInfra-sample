
本リポジトリは就職活動のポートフォリオ用として現行のホームラボ環境を構成する際に使用しているサンプルファイルを公開する目的で作成したものです。<br>
(技術スタック:Linux[Debian系],Ansible,K3S[Kubernetes])<br>
[ホスト構成]<br>
※コストの都合で現時点ではK3S(Kubernetes)ではシングルノード構成で構築し、家内DNS、DHCP、DBサーバー(サービス)はアクティブスタンバイ構成で構築。<br>
将来的にはK3S(Kubernetes)はマルチノード構成で構築しつつ、可能な限り各種サーバー(サービス)の可用性を向上させる予定。<br>
・[Raspberry Pi 4 Model B 4GB]x2 (K3S [ワーカー兼用]マスターノード、ワーカーノード[本番])<br>
・[VMware Workstation Player(amd64環境、ゲストOS:Debian 13 [Trixie]) ] (K3Sワーカーノード[テスト用])<br>

