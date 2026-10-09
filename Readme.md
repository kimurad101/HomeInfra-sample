
本リポジトリは就職活動のポートフォリオ用として現行のホームラボ環境を構成する際に使用しているサンプルファイルを公開する目的で作成したものです。<br>
(技術スタック:Linux[Debian系],Ansible,K3S[Kubernetes])<br>
[ホスト構成]<br>
※コストの都合で現時点ではK3S(Kubernetes)ではシングルノード構成で構築し、家内DNS、DHCP、DBサーバー(サービス)のみアクティブスタンバイ構成で構築。将来的にはK3S(Kubernetes)はマルチノード構成で構築しつつ、可能な限り各種サーバー(サービス)の可用性を向上させる予定。<br>
・[Raspberry Pi 4 Model B 4GB (arm64環境、OS:Raspberry Pi OS[Debian 13 (Trixie)])]x2 :(K3S [ワーカー兼用]マスターノード、ワーカーノード[本番])<br>
・[VMware Workstation Player(amd64環境、ゲストOS:Debian 13 [Trixie]) ] (K3Sワーカーノード[テスト用])<br>
<br>
[用途]<br>
※([進捗]用途:[技術スタック]:担当ノード)<br>
・[予定]DHCPサーバー:[Kea DHCP]:(アクティブスタンバイ構成[ワーカー兼用マスター,ワーカー])<br>
・[構築中]DBサーバー:[MariaDB-Operator & MaxScale]:(非同期レプリケーション[アクティブスタンバイ]構成[ワーカー兼用マスター,ワーカー])<br>
・[予定]DNSサーバー:[CoreDNS]:(アクティブスタンバイ構成[ワーカー兼用マスター,ワーカー])<br>
・[予定]ホームオートメーションサービス:[HomeAssistant]:[ワーカー]<br>
・[予定]VPNサーバー:[wireguard?]:[ワーカー]<br>
・[予定]内部向けWebサーバー:[Apache&PHP]:[ワーカー]<br>
・[予定]外部向けWebサーバー:[Nginx]:[ワーカー]<br>
・[予定]IoT/APIサーバー:[Python FastAPI]:[ワーカー]<br>
・[予定]ネットワークカメラレコーダー(防犯カメラ中継/録画サーバー):[go2rtc]:[ワーカー]<br>
<br>
