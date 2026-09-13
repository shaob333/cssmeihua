 <h1>Debian DDNS 一键脚本</h1>
 <ul>
<li>支持多域名解析。（注：如果域名超过两个，即三个以及三个以上，最好将ddns的时间调整至2分钟及两分钟以上）</li>
<li>支持自定义ddns时间，Debian默认一分钟，alpine默认两分钟。</li>
<li>支持Alpine、Debian。</li>
<li>支持 Cloudflare：利用 Cloudflare API，自动更新指定域名的 DNS 记录。</li>
<li>支持 IPv4 和 IPv6 双栈解析：可自动检测并更新网络的 IPv4 和 IPv6 地址。</li>
<li>IPv4 和 IPv6 域名独立解析：支持 IPv4 和 IPv6 域名的分开解析。</li>
<li>Telegram 通知：集成了 Telegram 通知功能，在 IP 变更时实时发送消息。</li>
<li>脚本完全开源，可自行查看。</li>
</ul>
<h1 id="部署">部署</h1>
<h2 id="准备">准备</h2>
<ul>
<li>cloudflare 全局token <a href="https://dash.cloudflare.com/profile/api-tokens">API 令牌 | Cloudflare</a></li>
<li>cloudflare 注册邮箱</li>
<li>一个可以DDns解析的域名</li>
<li>telegram bot api token （可选）</li>
<li>telegram user chat id （可选）</li>
</ul>
<p>在部署前需要在cloudflare里解析一个域名，根据需求解析A记录或者AAAA记录，如需双栈则需同时解析A记录和AAAA记录，A记录和AAAA记录可为同一个二级域名下不同的三级域名，例 ipv4.1.com ipv6.1.com 。</p>
<p><img src="/upload/image-bdlv.png" alt="image-bdlv.png" sizes="(max-width: 640px) 94vw, (max-width: 768px) 92vw, (max-width: 1024px) 88vw, min(800px, 85vw)" srcset="/upload/image-bdlv.png?width=1200 1200w, /upload/image-bdlv.png?width=800 800w, /upload/image-bdlv.png?width=1600 1600w, /upload/image-bdlv.png?width=400 400w" /></p>
<h2 id="一键脚本">一键脚本</h2>
<pre><code>bash &lt;(wget -qO- https://raw.githubusercontent.com/mocchen/cssmeihua/mochen/shell/ddns.sh)
</code></pre>
