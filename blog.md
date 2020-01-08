---
layout: blog
title: "blog"
permalink: /blog/
---

<a class="wannartclass" href="https://wannart.com/author/md" target="_blank"> @wannart&#x2665; </a> <br class="aclass">
<a class="wannartclass" href="https://medium.com/mucahiddogan_" target="_blank"> @medium </a>

* <a href="https://www.wannart.com/?p=170389" target="_blank"> Koca Yaşlı Şişko </a>
* <a href="https://medium.com/@mucahiddogan_/belki-de-her-şeye-yeniden-8398c6fc3796" target="_blank"> Belki de her şeye yeniden </a>
* <a href="https://medium.com/@mucahiddogan_/İyi-kodladık-kodla17-17d9f735aec2" target="_blank"> İyi kodla dık #kodla17 </a>
* <a href="https://medium.com/@mucahiddogan_/ktusec-kahvaltı-minictf-çözümmleri-c07ea71aed31" target="_blank">KtuSec Kahvaltı miniCTF çözümleri</a>
* <a href="https://medium.com/@mucahiddogan_/bilmök-2017-ve-konya-dd05766a2d6c" target="_blank"> Bilmök 2017 ve Konya </a>

<ul class="posts">
    {% for post in site.categories.blog %}
        <li>
            <span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
            ::
            <a class="post-link" href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
            @ {
            {% assign tag = post.tags | sort %}
            {% for category in tag %}<span><a href="{{ site.baseurl }}category/#{{ category }}" class="reserved">{{ category }}</a>{% if forloop.last != true %},{% endif %}</span>{% endfor %}
            {% assign tag = nil %}
            }
        </li>
    {% endfor %}
</ul>
<style>
    .aclass{
        margin: 5px;
    }
    .wannartclass{
        font-size: 15px;
    }
</style>
