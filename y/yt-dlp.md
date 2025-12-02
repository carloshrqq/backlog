#review #youtube 

# Massive forking m3u8

```text

//definir o caminho
cd "D:\Y\yt-dlp\rocketseat\node JS"

/**
* --cookies-from-browser=firefox   Carrega os cookies do firefox
*                                  solução do erro
*                                  "Sign in to confirm you're not a bot"
* -o
* -x                               audio only
*/

yt-dlp --cookies-from-browser=firefox -o "001 Iniciando com node js Introdução " https://b-vz-762f4670-e04.tv.pandavideo.com.br/2e1b574a-f24d-4e15-a0ef-2988c5d79b24/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "004 Criando um projeto Node" https://b-vz-762f4670-e04.tv.pandavideo.com.br/75a6d9b5-c984-4c78-a30d-b6d3df6f835a/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "005 node --watch" https://b-vz-762f4670-e04.tv.pandavideo.com.br/59ca113c-f654-4f91-a510-8cd0a80910da/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "006 Rotas de criação e listagem (Métodos HTTP)" https://b-vz-762f4670-e04.tv.pandavideo.com.br/83f7f25a-2ee7-4f20-996a-c467c3fffeb1/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "007 Salvando usuários em memória (Headers)" https://b-vz-762f4670-e04.tv.pandavideo.com.br/798508b8-d31a-410c-acb6-ab19d78cee0d/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "008 Conhecendo HTTP status codes" https://b-vz-762f4670-e04.tv.pandavideo.com.br/9ea01cb7-faa9-4b29-99c7-00e932314e23/playlist.m3u8

yt-dlp --cookies-from-browser=firefox -o "009 Entendendo Streams no Node" https://b-vz-762f4670-e04.tv.pandavideo.com.br/70c534a7-0bfa-47a8-9b25-e817a328c2bc/playlist.m3u8

```

# "Sign in to confirm you're not a bot" exploring solution

[YT-DLP Error: "Sign in to confirm you’re not a bot. This helps protect our community". Proxy recommendation](https://www.reddit.com/r/youtubedl/comments/1e6bzu4/ytdlp_error_sign_in_to_confirm_youre_not_a_bot/?rdt=39026)

https://github.com/yt-dlp/yt-dlp/issues/7811

download de videos grandes provavelmente ocasionou no erro 403

# SOLVED for 403 forbidden

[Error 403 on YT](https://www.reddit.com/r/youtubedl/comments/1hkp2si/error_403_on_yt/)

Comandos de atualização

`pip install yt-dlp --upgrade`
`python.exe -m pip install --upgrade pip`


Comando para download do vídeo

yt-dlp -4 -x URL

-x para subtrair somente o audio

<hr>

Well, here is my current solution as suggested by someone on the yt-dlp Github repo:

Log in to your Youtube account.

Export cookies from the browser you use to a text file as follows:

yt-dlp --cookies-from-browser firefox --cookies cookie.txt

3) Pass cookies to yt-dlp as follows: --cookies ./cookie.txt

In Media Downloader or which ever GUI front end to yt-dlp you use, find the way to change the configuration of the options passed to yt-dlp when your down loader runs yt-dlp. In Media Downloader, this can be done using the Configure tab and the "Engine Default Options" tab; copy the existing options, edit to add the option to pass cookies as above, then add, make the new configuration the default and save.

I tested this and Media Downloader can now download Youtube videos again. Until Youtube fucks it up again, of course, which could happen at any time.

I suspect what we really need in these days of AI is an AI that can use the browser to view a list of Youtube URLs one at a time, detect and remove the ads, and record and download the video. In other words, an AI that can essentially replicate what a real user does and do it undetectably by Youtube. AIs can already view and summarize Youtube videos, so I suspect such a solution (hopefully a locally run free one) will emerge eventually.

# Multiple link video multiline command 25-1

