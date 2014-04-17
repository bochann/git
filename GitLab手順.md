gitLab 進行手順

①　管理者にアカウントを作成してもらう。

②　ログインしたらRSA公開鍵をgitlabに登録

	＄ssh-keygen -t rsa
	
③　"~/.ssh/id_rsa.pub"に鍵が生成されるので、公開鍵の中身をまるっとすべてSSH Keysに登録

④　~/.ssh/config"に次の設定を書きたしておく。xxx.xxx.xxx.xxxのところにはGitLabサーバーのIPアド　　レス入れてね。DNSで解決できるならホスト名でも。


    Host gitlab-serverHostName xxx.xxx.xxx.xxxIdentifyFile ~/.ssh/id_rsa
    
※何故か公開鍵になってたので修正
あと、configは書かなくてもデフォルトでid_rsaを秘密鍵として使うみたいなので、秘密鍵がひとつだけ、って人はこれ書かなくてもいいみたいです。