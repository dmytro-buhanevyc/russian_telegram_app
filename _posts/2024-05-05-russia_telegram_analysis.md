---
layout: post
title: "Russia Telegram Analysis - 2024-05-05"
author: "Dmytro Bukhanevych"
categories: analysis
tags: [telegram, analysis]
image: daniel-olah-KDCzAGuf0e8-unsplash.jpg
permalink: "/analysis/russia-telegram-analysis-2024-05-05"
---

<style>
    /* Adjusting iframe-container styles */
    .wide-iframe-container {
        width: calc(100% + 30vw);  /* Extending the width */
        margin-left: -15vw;       /* Negative margin to push to the left */
        overflow: hidden;         /* In case the iframe content spills over */
    }

    .wide-iframe-container iframe {
        width: 100%;  /* Making the iframe take the full width of its container */
        border: none; /* Removing any borders from the iframe */
    }

    /* Toggle mechanism */
    .hidden {
        display: none;
    }
    
    .show-content-target:checked + .show-content {
        display: block;
    }
</style>

<h2>Main Topics</h2>
<p>Загалом було проаналізовано 6277 постів у Telegram за 04.05.2024. Було відстежено активність 112 найбільш популярних Telegram каналів у Росії. Після попередньої обробки, фільтрування за ключовими словами, кластеризації та зменшення шуму, 842 текстів було проаналізовано у крайньому звітному періоді.</p>
<!-- Embedding Main Plotly Visualization -->
<div class="wide-iframe-container">
    <iframe src="{{site.baseurl}}/visualizations/2024-05-05/fig_topics_time.html" height="850"></iframe>
</div>


<h2>Cluster Text</h2>

<!-- Dropdown to select a cluster -->
<select id="clusterSelector" onchange="displayClusterText()">
<option value="0">Cluster 0</option><option value="1">Cluster 1</option><option value="2">Cluster 2</option><option value="3">Cluster 3</option><option value="4">Cluster 4</option><option value="5">Cluster 5</option><option value="6">Cluster 6</option><option value="7">Cluster 7</option><option value="8">Cluster 8</option><option value="9">Cluster 9</option><option value="10">Cluster 10</option>
</select>

<!-- Display area for the selected cluster's text -->
<div id="clusterTextDisplay" class="hidden"></div>

<script type="text/javascript">
    var clusterDetails = {"0": "<b>Total Posts:</b> 112<br><b>Date:</b> 2024-05-04 12:45:06+00:00<br><b>Author:</b> rusbrief<br><b>Link:</b> https://t.me/s/rusbrief/226847<br><b>Subscribers:</b> 534519<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u0411\u0440\u0438\u0444\u0438\u043d\u0433-1. \u0412\u043b\u0430\u0434\u0438\u043c\u0438\u0440 \u0417\u0435\u043b\u0435\u043d\u0441\u043a\u0438\u0439 \u0441\u0442\u0430\u043b \u0432\u0442\u043e\u0440\u044b\u043c \u0433\u043b\u0430\u0432\u043e\u0439 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432\u0430, \u043e\u0431\u044a\u044f\u0432\u043b\u0435\u043d\u044b\u043c \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u041c\u0412\u0414 \u0420\u043e\u0441\u0441\u0438\u0438. \u0420\u0430\u043d\u0435\u0435 \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u0431\u044b\u043b\u0430 \u043e\u0431\u044a\u044f\u0432\u043b\u0435\u043d\u0430 \u043f\u0440\u0435\u043c\u044c\u0435\u0440-\u043c\u0438\u043d\u0438\u0441\u0442\u0440 \u042d\u0441\u0442\u043e\u043d\u0438\u0438 \u041a\u0430\u043b\u043b\u0430\u0441. \u041f\u0440\u0430\u043a\u0442\u0438\u043a\u0430 \u043e\u0431\u044a\u044f\u0432\u043b\u0435\u043d\u0438\u044f \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u0434\u0435\u0439\u0441\u0442\u0432\u0443\u044e\u0449\u0438\u0445 \u0433\u043b\u0430\u0432 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432 \u0438 \u043f\u0440\u0430\u0432\u0438\u0442\u0435\u043b\u044c\u0441\u0442\u0432 \u0438\u043d\u043e\u0441\u0442\u0440\u0430\u043d\u043d\u044b\u0445 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432 \u043f\u0440\u043e\u0442\u0438\u0432\u043e\u0440\u0435\u0447\u0438\u0442  \u043c\u0435\u0436\u0434\u0443\u043d\u0430\u0440\u043e\u0434\u043d\u043e\u043c\u0443 \u0441\u0442\u0430\u0442\u0443\u0441\u0443 \u044d\u043a\u0441\u0442\u0435\u0440\u0440\u0438\u0442\u043e\u0440\u0438\u0430\u043b\u044c\u043d\u043e\u0441\u0442\u0438 \u0438 \u0437\u0430\u043a\u043e\u043d\u0430\u043c \u0420\u0424. \u041d\u043e \u0420\u043e\u0441\u0441\u0438\u044f \u0434\u0435\u043c\u043e\u043d\u0441\u0442\u0440\u0430\u0442\u0438\u0432\u043d\u043e \u0438\u0445 \u043d\u0430\u0440\u0443\u0448\u0430\u0435\u0442. \u041f\u043e \u043c\u043d\u0435\u043d\u0438\u044e \u044e\u0440\u0438\u0441\u0442\u043e\u0432, \u0420\u043e\u0441\u0441\u0438\u044f \u043f\u043e\u0441\u043b\u0435 \u043e\u0440\u0434\u0435\u0440\u0430 \u041c\u0423\u0421 \u043d\u0430 \u0430\u0440\u0435\u0441\u0442 \u041f\u0443\u0442\u0438\u043d\u0430 \u0434\u0435-\u0444\u0430\u043a\u0442\u043e \u0432\u044b\u0448\u043b\u0430 \u0438\u0437 \u043c\u0435\u0436\u0434\u0443\u043d\u0430\u0440\u043e\u0434\u043d\u043e\u0433\u043e \u0441\u0442\u0430\u0442\u0443\u0441\u0430 \u043e \u043f\u0440\u0438\u0437\u043d\u0430\u043d\u0438\u0438 \u043d\u0435\u043f\u0440\u0438\u043a\u043e\u0441\u043d\u043e\u0432\u0435\u043d\u043d\u043e\u0441\u0442\u0438 \u0433\u043b\u0430\u0432 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432 \u0438 \u043f\u0440\u0435\u0434\u0441\u0442\u0430\u0432\u0438\u0442\u0435\u043b\u0435\u0439 \u0432\u043b\u0430\u0441\u0442\u0438 \u0438\u043d\u043e\u0441\u0442\u0440\u0430\u043d\u043d\u044b\u0445 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432. \u0424\u0430\u043a\u0442\u0438\u0447\u0435\u0441\u043a\u0438 \u044d\u0442\u043e \u043e\u0437\u043d\u0430\u0447\u0430\u0435\u0442,\u0447\u0442\u043e \u0420\u043e\u0441\u0441\u0438\u044f \u043f\u043e\u0437\u0432\u043e\u043b\u044f\u0435\u0442 \u0441\u0435\u0431\u0435 \u0430\u0440\u0435\u0441\u0442\u043e\u0432\u0430\u0442\u044c \u043b\u044e\u0431\u043e\u0433\u043e \u0433\u043b\u0430\u0432\u0443 \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432\u0430 \u0438\u043b\u0438 \u043f\u0440\u0435\u0434\u0441\u0442\u0430\u0432\u0438\u0442\u0435\u043b\u044f \u0432\u043b\u0430\u0441\u0442\u0438 \u0438\u043d\u043e\u0441\u0442\u0440\u0430\u043d\u043d\u043e\u0433\u043e \u0433\u043e\u0441\u0443\u0434\u0430\u0440\u0441\u0442\u0432\u0430. \u042d\u0442\u043e \u043c\u043e\u0436\u0435\u0442 \u043f\u043e\u0432\u043b\u0435\u0447\u044c \u0440\u0435\u0437\u043a\u043e\u0435 \u043e\u0433\u0440\u0430\u043d\u0438\u0447\u0435\u043d\u0438\u0435 \u043f\u043e\u0435\u0437\u0434\u043e\u043a \u0438\u043d\u043e\u0441\u0442\u0440\u0430\u043d\u043d\u044b\u0445 \u0434\u0435\u043b\u0435\u0433\u0430\u0446\u0438\u0439 \u0432 \u0420\u043e\u0441\u0441\u0438\u044e. @rusbri", "1": "<b>Total Posts:</b> 24<br><b>Date:</b> 2024-05-04 21:20:57+00:00<br><b>Author:</b> petrovtel<br><b>Link:</b> https://t.me/s/petrovtel/54141<br><b>Subscribers:</b> 566725<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u041f\u0443\u0442\u0438\u043d \u0438 \u0421\u043e\u0431\u044f\u043d\u0438\u043d \u043f\u0440\u0438\u0431\u044b\u043b\u0438 \u0432 \u0425\u0440\u0430\u043c \u0425\u0440\u0438\u0441\u0442\u0430 \u0421\u043f\u0430\u0441\u0438\u0442\u0435\u043b\u044f \u043d\u0430 \u043f\u0430\u0441\u0445\u0430\u043b\u044c\u043d\u043e\u0435 \u0431\u043e\u0433\u043e\u0441\u043b\u0443\u0436\u0435\u043d\u0438\u0435, \u2014 \u0421\u041c\u0418\u041a\u041a \ud83d\udc00", "2": "<b>Total Posts:</b> 48<br><b>Date:</b> 2024-05-04 14:43:32+00:00<br><b>Author:</b> solovievlive<br><b>Link:</b> https://t.me/s/SolovievLive/255691<br><b>Subscribers:</b> 1335130<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u2757\ufe0f\u041c\u0412\u0414 \u0420\u0424 \u043e\u0431\u044a\u044f\u0432\u0438\u043b\u043e \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u043a\u043e\u043c\u0430\u043d\u0434\u0443\u044e\u0449\u0435\u0433\u043e \u0441\u0443\u0445\u043e\u043f\u0443\u0442\u043d\u044b\u043c\u0438 \u0432\u043e\u0439\u0441\u043a\u0430\u043c\u0438 \u0412\u0421\u0423 \u0410\u043b\u0435\u043a\u0441\u0430\u043d\u0434\u0440\u0430 \u041f\u0430\u0432\u043b\u044e\u043a\u0430\u0420\u0430\u043d\u0435\u0435 \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u0431\u044b\u043b\u0438 \u043e\u0431\u044a\u044f\u0432\u043b\u0435\u043d\u044b \u043d\u044b\u043d\u0435\u0448\u043d\u0438\u0439 \u0438 \u0431\u044b\u0432\u0448\u0438\u0439 \u043f\u0440\u0435\u0437\u0438\u0434\u0435\u043d\u0442\u044b \u0423\u043a\u0440\u0430\u0438\u043d\u044b \u2014 \u0412\u043b\u0430\u0434\u0438\u043c\u0438\u0440 \u0417\u0435\u043b\u0435\u043d\u0441\u043a\u0438\u0439 \u0438 \u041f\u0435\u0442\u0440 \u041f\u043e\u0440\u043e\u0448\u0435\u043d\u043a\u043e.\u041f\u043e\u0434\u043f\u0438\u0441\u044b\u0432\u0430\u0439\u0441\u044f \u043d\u0430 Telegram \u0421\u041e\u041b\u041e\u0412\u042c\u0401\u0412!", "3": "<b>Total Posts:</b> 23<br><b>Date:</b> 2024-05-04 06:14:25+00:00<br><b>Author:</b> ukraina_ru<br><b>Link:</b> https://t.me/s/ukraina_ru/198878<br><b>Subscribers:</b> 411999<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u26a1 \u0411\u043b\u0430\u0433\u0438\u0435 \u0432\u0435\u0441\u0442\u0438 \u0441 \u0414\u043e\u043d\u0435\u0446\u043a\u043e\u0433\u043e \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u044f\u041d\u0430\u0441\u0435\u043b\u0435\u043d\u043d\u044b\u0439 \u043f\u0443\u043d\u043a\u0442 \u0410\u0440\u0445\u0430\u043d\u0433\u0435\u043b\u044c\u0441\u043a\u043e\u0435 \u043e\u0441\u0432\u043e\u0431\u043e\u0436\u0434\u0451\u043d \u043e\u0442 \u043c\u043d\u043e\u0433\u043e\u043b\u0435\u0442\u043d\u0435\u0439 \u043e\u043a\u043a\u0443\u043f\u0430\u0446\u0438\u0438 \u043f\u0440\u043e\u0442\u0438\u0432\u043d\u0438\u043a\u0430.\u0412\u0440\u0430\u0436\u0435\u0441\u043a\u0430\u044f \u043e\u0431\u043e\u0440\u043e\u043d\u0430 \u043f\u0430\u043b\u0430, \u043e\u043f\u0430\u0441\u0430\u044f\u0441\u044c \u043e\u043a\u0440\u0443\u0436\u0435\u043d\u0438\u044f \u043f\u043e\u0434\u0440\u0430\u0437\u0434\u0435\u043b\u0435\u043d\u0438\u044f \u0412\u0421\u0423 \u043d\u0435\u0441\u043a\u043e\u043b\u044c\u043a\u043e \u0434\u043d\u0435\u0439 \u043d\u0430\u0437\u0430\u0434 \u043d\u0430\u0447\u0430\u043b\u0438 \u043e\u0442\u0441\u0442\u0443\u043f\u043b\u0435\u043d\u0438\u0435 \u0432 \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438 \u041a\u0430\u043b\u0438\u043d\u043e\u0432\u0441\u043a\u043e\u0433\u043e \u043f\u0440\u0443\u0434\u0430, \u0430 \u0442\u0430\u043a\u0436\u0435 \u043e\u0442\u0447\u0430\u0441\u0442\u0438 \u0432 \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438 \u043d.\u043f. \u041d\u043e\u0432\u043e\u0430\u043b\u0435\u043a\u0441\u0430\u043d\u0434\u0440\u043e\u0432\u043a\u0430.\u0412\u0447\u0435\u0440\u0430, \u0432 \u043f\u0440\u043e\u0446\u0435\u0441\u0441\u0435 \u043e\u0442\u0441\u0442\u0443\u043f\u043b\u0435\u043d\u0438\u044f \u0432\u0440\u0430\u0433 \u043f\u043e\u043d\u0435\u0441 \u043e\u0449\u0443\u0442\u0438\u043c\u044b\u0435 \u043f\u043e\u0442\u0435\u0440\u0438, \u0442\u0430\u043a \u043a\u0430\u043a \u043f\u043e \u043e\u0442\u0441\u0442\u0443\u043f\u0430\u044e\u0449\u0438\u043c \u0433\u0440\u0443\u043f\u043f\u0430\u043c \u043f\u0440\u043e\u0442\u0438\u0432\u043d\u0438\u043a\u0430 \u0431\u044b\u043b \u043e\u0442\u043a\u0440\u044b\u0442 \u043c\u0430\u0441\u0441\u0438\u0440\u043e\u0432\u0430\u043d\u043d\u044b\u0439 \u043e\u0433\u043e\u043d\u044c \u0438\u0437 \u0430\u0440\u0442\u0438\u043b\u043b\u0435\u0440\u0438\u0438, \u0434\u043e\u043a\u043b\u0430\u0434\u044b\u0432\u0430\u0435\u0442 \u041d\u0433\u041f \u0440\u0430ZV\u0435\u0434\u043a\u0430.\u0414\u043e\u043b\u0433\u043e \u0443\u0434\u0435\u0440\u0436\u0438\u0432\u0430\u0442\u044c \u0434\u0430\u043b\u044c\u043d\u0435\u0439\u0448\u0435\u0435 \u043d\u0430\u0441\u0442\u0443\u043f\u043b\u0435\u043d\u0438\u0435 \u0412\u0421 \u0420\u0424 \u0432 \u0440\u0430\u0439\u043e\u043d\u0435 \u043d.\u043f. \u041a\u0430\u043b\u0438\u043d\u043e\u0432\u043e \u0432\u0440\u0430\u0433 \u043d\u0435 \u0441\u043c\u043e\u0436\u0435\u0442, \u0442\u0430\u043a \u043a\u0430\u043a \u043e\u0441\u043d\u043e\u0432\u043d\u044b\u0435 \u0444\u043e\u0440\u0442\u0438\u0444\u0438\u043a\u0430\u0446\u0438\u043e\u043d\u043d\u044b\u0435 \u0441\u043e\u043e\u0440\u0443\u0436\u0435\u043d\u0438\u044f \u0432\u043e\u0437\u0432\u043e\u0434\u0438\u043b \u0432 \u043d\u0430\u0441\u0435\u043b\u0435\u043d\u043d\u043e\u043c \u043f\u0443\u043d\u043a\u0442\u0435 \u041d\u043e\u0432\u043e\u0430\u043b\u0435\u043a\u0441\u0430\u043d\u0434\u0440\u043e\u0432\u043a\u0430, \u0432 \u0440\u0430\u0439\u043e\u043d\u0435 \u043a\u043e\u0442\u043e\u0440\u043e\u0433\u043e \u0438 \u043f\u043e\u043f\u044b\u0442\u0430\u0435\u0442\u0441\u044f \u043e\u0441\u0442\u0430\u043d\u043e\u0432\u0438\u0442\u044c \u043d\u0430\u0448\u0435 \u043d\u0430\u0441\u0442\u0443\u043f\u043b\u0435\u043d\u0438\u0435. \u0412\u0441\u0435 \u0431\u0443\u0434\u0435\u0442 \u0442\u0430\u043a, \u043a\u0430\u043a \u043d\u0443\u0436\u043d\u043e \u0420\u043e\u0441\u0441\u0438\u0438! \u0416\u0434\u0435\u043c \u043e\u0444\u0438\u0446\u0438\u0430\u043b\u044c\u043d\u043e\u0433\u043e \u043f\u043e\u0434\u0442\u0432\u0435\u0440\u0436\u0434\u0435\u043d\u0438\u044f!", "4": "<b>Total Posts:</b> 75<br><b>Date:</b> 2024-05-04 21:59:59+00:00<br><b>Author:</b> ukraina_ru<br><b>Link:</b> https://t.me/s/ukraina_ru/199020<br><b>Subscribers:</b> 411999<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \ud83d\udc4d \u0422\u0440\u0430\u0434\u0438\u0446\u0438\u043e\u043d\u043d\u044b\u0435 \u0438\u0442\u043e\u0433\u0438 \u0434\u043d\u044f \u0434\u043b\u044f \u043f\u043e\u0434\u043f\u0438\u0441\u0447\u0438\u043a\u043e\u0432 \u043a\u0430\u043d\u0430\u043b\u0430 \u0423\u043a\u0440\u0430\u0438\u043d\u0430.\u0440\u0443\u2705 \u041d\u0430 \u0417\u0430\u043a\u0430\u0440\u043f\u0430\u0442\u044c\u0435 \u043f\u0440\u043e\u0438\u0437\u043e\u0448\u0435\u043b \u043a\u043e\u043d\u0444\u043b\u0438\u043a\u0442 \u043c\u0435\u0441\u0442\u043d\u044b\u0445 \u0436\u0438\u0442\u0435\u043b\u0435\u0439 \u0441 \u0422\u0426\u041a\u0448\u043d\u0438\u043a\u0430\u043c\u0438, \u043a\u043e\u0442\u043e\u0440\u044b\u0439 \u0437\u0430\u043a\u043e\u043d\u0447\u0438\u043b\u0441\u044f \u0441\u0442\u0440\u0435\u043b\u044c\u0431\u043e\u0439;\u2705 \u041d\u0430 \u0410\u0432\u0434\u0435\u0435\u0432\u0441\u043a\u043e\u043c \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438 \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0435\u043d \u0435\u0449\u0451 \u043e\u0434\u0438\u043d M1A1 \u201cAbrams\u201d; \u2705 \u0421\u0442\u0443\u0434\u0435\u043d\u0442\u044b \u0438 \u0430\u0441\u043f\u0438\u0440\u0430\u043d\u0442\u044b \u0432\u0443\u0437\u043e\u0432 \u0431\u0443\u0434\u0443\u0442 \u0432\u044b\u043d\u0443\u0436\u0434\u0435\u043d\u044b \u0441\u0434\u0430\u0432\u0430\u0442\u044c \u043f\u0440\u043e\u043c\u0435\u0436\u0443\u0442\u043e\u0447\u043d\u044b\u0439 \u044d\u043a\u0437\u0430\u043c\u0435\u043d, \u0447\u0442\u043e\u0431\u044b \u0432\u043b\u0430\u0441\u0442\u0438 \u0432\u044b\u044f\u0432\u0438\u043b\u0438 \u0433\u0440\u0430\u0436\u0434\u0430\u043d, \u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u044f\u043a\u043e\u0431\u044b \u0443\u043a\u043b\u043e\u043d\u044f\u044e\u0442\u0441\u044f \u043e\u0442 \u043c\u043e\u0431\u0438\u043b\u0438\u0437\u0430\u0446\u0438\u0438;\u2705 \u041c\u0412\u0414 \u0420\u0424 \u043e\u0431\u044a\u044f\u0432\u0438\u043b\u043e \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u0417\u0435\u043b\u0435\u043d\u0441\u043a\u043e\u0433\u043e \u043f\u043e \u0443\u0433\u043e\u043b\u043e\u0432\u043d\u043e\u0439 \u0441\u0442\u0430\u0442\u044c\u0435;\u2705 \u0412\u0441\u043b\u0435\u0434 \u0437\u0430 \u0417\u0435\u043b\u0435\u043d\u0441\u043a\u0438\u043c \u0432 \u0440\u043e\u0437\u044b\u0441\u043a \u043e\u0431\u044a\u044f\u0432\u0438\u043b\u0438 \u041f\u0435\u0442\u0440\u0430 \u041f\u043e\u0440\u043e\u0448\u0435\u043d\u043a\u043e, \u043a\u043e\u043c\u0430\u043d\u0434\u0443\u044e\u0449\u0435\u0433\u043e \u0441\u0443\u0445\u043e\u043f\u0443\u0442\u043d\u044b\u043c\u0438 \u0432\u043e\u0439\u0441\u043a\u0430\u043c\u0438 \u0412\u0421\u0423 \u0410\u043b\u0435\u043a\u0441\u0430\u043d\u0434\u0440\u0430 \u041f\u0430\u0432\u043b\u044e\u043a\u0430, \u0431\u044b\u0432\u0448\u0435\u0433\u043e \u0438.\u043e. \u043c\u0438\u043d\u0438\u0441\u0442\u0440\u0430 \u043e\u0431\u043e\u0440\u043e\u043d\u044b \u0423\u043a\u0440\u0430\u0438\u043d\u044b \u0438 \u043d\u044b\u043d\u0435\u0448\u043d\u0435\u0433\u043e \u0440\u0443\u043a\u043e\u0432\u043e\u0434\u0438\u0442\u0435\u043b\u044f \u041d\u0430\u0446\u0438\u043e\u043d\u0430\u043b\u044c\u043d\u043e\u0433\u043e \u0443\u043d\u0438\u0432\u0435\u0440\u0441\u0438\u0442\u0435\u0442\u0430 \u043e\u0431\u043e\u0440\u043e\u043d\u044b \u0423\u043a\u0440\u0430\u0438\u043d\u044b \u041c\u0438\u0445\u0430\u0438\u043b\u0430 \u041a\u043e\u0432\u0430\u043b\u044f; \u2705 \u0412 \u0446\u0435\u043d\u0442\u0440\u0435 \u041c\u043e\u0441\u043a\u0432\u044b \u043e\u0446\u0435\u043f\u0438\u043b\u0438 \u043c\u0430\u0448\u0438\u043d\u0443 \u0441 \u0440\u0430\u0437\u043e\u0431\u0440\u0430\u043d\u043d\u044b\u043c \u0431\u0435\u0441\u043f\u0438\u043b\u043e\u0442\u043d\u0438\u043a\u043e\u043c \u0441\u0430\u043c\u043e\u043b\u0451\u0442\u043d\u043e\u0433\u043e \u0442\u0438\u043f\u0430;\u2705 \u041f\u043e\u0447\u0442\u0438 87% \u0443\u043a\u0440\u0430\u0438\u043d\u0446\u0435\u0432 \u0434\u043e \u0441\u0438\u0445 \u043f\u043e\u0440 \u043d\u0435 \u0443\u0441\u0442\u0440\u043e\u0438\u043b\u0438\u0441\u044c \u043d\u0430 \u0440\u0430\u0431\u043e\u0442\u0443 \u0432 \u0413\u0435\u0440\u043c\u0430\u043d\u0438\u0438; \u2705 \u0418\u0442\u0430\u043b\u0438\u044f \u0438\u0441\u043a\u043b\u044e\u0447\u0430\u0435\u0442 \u043f\u0440\u044f\u043c\u043e\u0435 \u0432\u043c\u0435\u0448\u0430\u0442\u0435\u043b\u044c\u0441\u0442\u0432\u043e \u0441\u0432\u043e\u0438\u0445 \u0432\u043e\u0435\u043d\u043d\u044b\u0445 \u0432 \u0443\u043a\u0440\u0430\u0438\u043d\u0441\u043a\u0438\u0439 \u043a\u043e\u043d\u0444\u043b\u0438\u043a\u0442;\u2705 \u0423\u043a\u0440\u0430\u0438\u043d\u0441\u043a\u0438\u0445 \u0430\u043b\u043a\u043e\u0433\u043e\u043b\u0438\u043a\u043e\u0432 \u0438 \u043d\u0430\u0440\u043a\u043e\u043c\u0430\u043d\u043e\u0432 \u0431\u0443\u0434\u0443\u0442 \u043c\u043e\u0431\u0438\u043b\u0438\u0437\u043e\u0432\u044b\u0432\u0430\u0442\u044c; \u2705 132 \u0431\u0440\u0438\u0433\u0430\u0434\u0430 \u0410\u0440\u043c\u0438\u0438 \u0420\u0424 1-\u0433\u043e \u0410\u041a \u043d\u0430 \u0413\u043e\u0440\u043b\u043e\u0432\u0441\u043a\u043e\u043c \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438 \u043e\u0441\u0432\u043e\u0431\u043e\u0434\u0438\u043b\u0438 \u0441\u0440\u0430\u0437\u0443 \u0442\u0440\u0438 \u043d\u0430\u0441\u0435\u043b\u0435\u043d\u043d\u044b\u0445 \u043f\u0443\u043d\u043a\u0442\u0430 - \u041d\u043e\u0432\u043e\u043a\u0430\u043b\u0438\u043d\u043e\u0432\u043e, \u041a\u0435\u0440\u0430\u043c\u0438\u043a, \u0410\u0440\u0445\u0430\u043d\u0433\u0435\u043b\u044c\u0441\u043a\u043e\u0435. \u0421\u043f\u043e\u043a\u043e\u0439\u043d\u043e\u0439 \u043d\u043e\u0447\u0438, \u0434\u043e\u0440\u043e\u0433\u0438\u0435 \u0434\u0440\u0443\u0437\u044c\u044f! \u041f\u043e\u0437\u0434\u0440\u0430\u0432\u043b\u044f\u0435\u043c \u0432\u0430\u0441 \u0441\u043e \u0421\u0432\u0435\u0442\u043b\u044b\u043c \u041f\u0440\u0430\u0437\u0434\u043d\u0438\u043a\u043e\u043c \u0425\u0440\u0438\u0441\u0442\u043e\u0432\u0430 \u0412\u043e\u0441\u043a\u0440\u0435\u0441\u0435\u043d\u0438\u044f! \u041c\u044b \u0437\u0430\u0441\u0442\u0443\u043f\u0430\u0435\u043c \u043d\u0430 \u043d\u043e\u0447\u043d\u043e\u0435 \u0434\u0435\u0436\u0443\u0440\u0441\u0442\u0432\u043e. \u0410 \u0435\u0441\u043b\u0438 \u0432\u0430\u043c, \u043a\u0430\u043a \u0438 \u043d\u0430\u043c, \u043d\u0435 \u0441\u043f\u0438\u0442\u0441\u044f, \u0442\u043e \u043f\u043e\u0447\u0438\u0442\u0430\u0439\u0442\u0435 \u044d\u043a\u0441\u043a\u043b\u044e\u0437\u0438\u0432\u043d\u044b\u0435 \u0430\u043d\u0430\u043b\u0438\u0442\u0438\u0447\u0435\u0441\u043a\u0438\u0435 \u043c\u0430\u0442\u0435\u0440\u0438\u0430\u043b\u044b \u043d\u0430 \u043d\u0430\u0448\u0435\u043c \u0432\u0442\u043e\u0440\u043e\u043c \u043a\u0430\u043d\u0430\u043b\u0435.\u0412\u0430\u0448\u0430 \u0423\u043a\u0440\u0430\u0438\u043d\u0430.\u0440\u0443 \ud83d\udc4d", "5": "<b>Total Posts:</b> 34<br><b>Date:</b> 2024-05-04 14:48:22+00:00<br><b>Author:</b> rvvoenkor<br><b>Link:</b> https://t.me/s/RVvoenkor/67414<br><b>Subscribers:</b> 1440943<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u203c\ufe0f\ud83c\uddf7\ud83c\uddfa\ud83c\uddfa\ud83c\udde6\u0410\u0440\u043c\u0438\u044f \u0420\u043e\u0441\u0441\u0438\u0438 \u0441\u0442\u0440\u0435\u043c\u0438\u0442\u0441\u044f \u0432\u044b\u0431\u0438\u0442\u044c \u041f\u0412\u041e \u0412\u0421\u0423 \u043f\u0435\u0440\u0435\u0434 \u043d\u043e\u0432\u044b\u043c \u043c\u0430\u0441\u0441\u0438\u0440\u043e\u0432\u0430\u043d\u043d\u044b\u043c \u0443\u0434\u0430\u0440\u043e\u043c, \u2014 \u0432\u043e\u0435\u043d\u043d\u044b\u0435 \u0412\u0421\u0423\u25aa\ufe0f\"\u0422\u0440\u0430\u0435\u043a\u0442\u043e\u0440\u0438\u044f \u0440\u0430\u043a\u0435\u0442, \u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u043b\u0435\u0442\u0435\u043b\u0438 \u0432 \u041e\u0434\u0435\u0441\u0441\u043a\u0443\u044e \u043e\u0431\u043b\u0430\u0441\u0442\u044c, \u0431\u044b\u043b\u0430 \u0447\u0435\u0440\u0435\u0437 \u0425\u0435\u0440\u0441\u043e\u043d\u0441\u043a\u0443\u044e \u043e\u0431\u043b\u0430\u0441\u0442\u044c - \u0434\u0430\u043b\u044c\u0448\u0435 \u0431\u044b\u0432\u0448\u0438\u0439 \u0421\u043d\u0438\u0433\u0438\u0440\u0451\u0432\u0441\u043a\u0438\u0439 \u0440\u0430\u0439\u043e\u043d \u041d\u0438\u043a\u043e\u043b\u0430\u0435\u0432\u0441\u043a\u043e\u0439 \u043e\u0431\u043b\u0430\u0441\u0442\u0438 - \u0412\u043e\u0437\u043d\u0435\u0441\u0435\u043d\u0441\u043a\u0438\u0439 \u0440\u0430\u0439\u043e\u043d \u041d\u0438\u043a\u043e\u043b\u0430\u0435\u0432\u0441\u043a\u043e\u0439 \u043e\u0431\u043b\u0430\u0441\u0442\u0438 - \u043f\u0435\u0440\u0435\u043b\u0451\u0442 \u043d\u0430 \u041e\u0434\u0435\u0441\u0441\u043a\u0443\u044e \u043e\u0431\u043b\u0430\u0441\u0442\u044c\", - \u043f\u0438\u0448\u0435\u0442 \u043e\u0434\u0438\u043d \u0438\u0437 \u0443\u043a\u0440\u0430\u0438\u043d\u0441\u043a\u0438\u0445 \u0432\u043e\u0435\u043d\u043d\u044b\u0445 \u0440\u0435\u0441\u0443\u0440\u0441\u043e\u0432.\u25aa\ufe0f\u0418\u0441\u043f\u043e\u043b\u044c\u0437\u043e\u0432\u0430\u043b\u0438\u0441\u044c \u043d\u0438\u0437\u043a\u043e\u043b\u0435\u0442\u044f\u0449\u0438\u0435 \"\u0418\u0441\u043a\u0430\u043d\u0434\u0435\u0440\u044b\" \u0438 \"\u041a\u0430\u043b\u0438\u0431\u0440\u044b\".\u00a0\u2796\"\u041e\u0431\u0441\u0442\u0440\u0435\u043b \u043e\u0436\u0438\u0434\u0430\u0435\u043c \u043d\u0430 \u0434\u043d\u044f\u0445. \u0426\u0435\u043b\u044c\u044e \u0431\u0443\u0434\u0435\u0442 \u0432 \u043e\u0447\u0435\u0440\u0435\u0434\u043d\u043e\u0439 \u0440\u0430\u0437 \u044d\u043d\u0435\u0440\u0433\u0435\u0442\u0438\u0447\u0435\u0441\u043a\u0430\u044f \u0438\u043d\u0444\u0440\u0430\u0441\u0442\u0440\u0443\u043a\u0442\u0443\u0440\u0430 \u0432 \u0440\u0430\u0437\u043d\u044b\u0445 \u043e\u0431\u043b\u0430\u0441\u0442\u044f\u0445 \u0441\u0442\u0440\u0430\u043d\u044b, \u0441 \u0443\u043f\u043e\u0440\u043e\u043c \u043d\u0430 \u0446\u0435\u043d\u0442\u0440\u0430\u043b\u044c\u043d\u044b\u0435 \u0438 \u0437\u0430\u043f\u0430\u0434\u043d\u044b\u0435 \u043e\u0431\u043b\u0430\u0441\u0442\u0438\", - \u043f\u0438\u0448\u0435\u0442 \u043e\u043d.t.me/RVvoenkor", "6": "<b>Total Posts:</b> 42<br><b>Date:</b> 2024-05-04 18:43:52+00:00<br><b>Author:</b> readovkanews<br><b>Link:</b> https://t.me/s/readovkanews/79276<br><b>Subscribers:</b> 2541285<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u0412 \u0425\u0430\u0440\u044c\u043a\u043e\u0432\u0435 \u0432\u043d\u043e\u0432\u044c \u043f\u0440\u043e\u0437\u0432\u0443\u0447\u0430\u043b\u0438 \u0432\u0437\u0440\u044b\u0432\u044b \u2014 \u0441\u0438\u0441\u0442\u0435\u043c\u0430 \u041f\u0412\u041e, \u043d\u0435\u043a\u043e\u0433\u0434\u0430 \u043e\u0431\u043e\u0440\u043e\u043d\u044f\u0432\u0448\u0430\u044f \u043e\u0431\u044a\u0435\u043a\u0442\u044b \u0412\u0421\u0423, \u0441\u0434\u0435\u0442\u043e\u043d\u0438\u0440\u043e\u0432\u0430\u043b\u0430 \u043f\u043e\u0441\u043b\u0435 \u0443\u0434\u0430\u0440\u0430 \u0440\u0443\u0441\u0441\u043a\u043e\u0439 \u0430\u0440\u043c\u0438\u0438\u0420\u0443\u0441\u0441\u043a\u0438\u0435 \u0431\u043e\u0439\u0446\u044b \u043f\u0440\u043e\u0434\u043e\u043b\u0436\u0430\u044e\u0442 \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0430\u0442\u044c \u0432\u0440\u0430\u0436\u0435\u0441\u043a\u0443\u044e \u0438\u043d\u0444\u0440\u0430\u0441\u0442\u0440\u0443\u043a\u0442\u0443\u0440\u0443 \u0432 \u0425\u0430\u0440\u044c\u043a\u043e\u0432\u0435. \u0421\u043e\u043e\u0431\u0449\u0430\u0435\u0442\u0441\u044f, \u0447\u0442\u043e \u0431\u044b\u043b \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0435\u043d \u0437\u0430\u043f\u0430\u0434\u043d\u044b\u0439 \u0437\u0435\u043d\u0438\u0442\u043d\u043e-\u0440\u0430\u043a\u0435\u0442\u043d\u044b\u0439 \u043a\u043e\u043c\u043f\u043b\u0435\u043a\u0441 \u041f\u0412\u041e \u0432 \u041d\u043e\u0432\u043e\u0431\u0430\u0432\u0430\u0440\u0441\u043a\u043e\u043c \u0440\u0430\u0439\u043e\u043d\u0435 \u0433\u043e\u0440\u043e\u0434\u0430. \u0421\u0435\u0440\u0438\u044f \u0434\u0435\u0442\u043e\u043d\u0430\u0446\u0438\u0439, \u043f\u043e\u0441\u043b\u0435\u0434\u0443\u044e\u0449\u0438\u0439 \u043f\u043e\u0436\u0430\u0440, \u0430 \u0442\u0430\u043a\u0436\u0435 \u0444\u043e\u0442\u043e\u0433\u0440\u0430\u0444\u0438\u0438, \u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u043f\u0443\u0431\u043b\u0438\u043a\u0443\u044e\u0442 \u043c\u0435\u0441\u0442\u043d\u044b\u0435 Telegram-\u043a\u0430\u043d\u0430\u043b\u044b, \u043f\u043e\u0434\u0442\u0432\u0435\u0440\u0436\u0434\u0430\u044e\u0442 \u0443\u0441\u043f\u0435\u0445 \u0430\u0442\u0430\u043a\u0438.\u00ab\u041f\u044f\u0442\u0438\u044d\u0442\u0430\u0436\u043a\u0430 \u0448\u0430\u0442\u0430\u043b\u0430\u0441\u044c \u043a\u0430\u043a \u043f\u0440\u043e\u043c\u043e\u043a\u0430\u0448\u043a\u0430\u00bb, \u2014 \u043f\u0438\u0448\u0443\u0442 \u0443\u043a\u0440\u0430\u0438\u043d\u0441\u043a\u0438\u0435 \u043a\u043e\u043c\u043c\u0435\u043d\u0442\u0430\u0442\u043e\u0440\u044b \u0432 \u043c\u0435\u0441\u0442\u043d\u044b\u0445 \u0421\u041c\u0418.\u0417\u0430 \u0441\u0443\u0442\u043a\u0438 \u044d\u0442\u043e \u0442\u0440\u0435\u0442\u0438\u0439 \u0440\u0435\u0437\u0443\u043b\u044c\u0442\u0430\u0442\u0438\u0432\u043d\u044b\u0439 \u0443\u0434\u0430\u0440 \u0412\u0421 \u0420\u0424 \u043f\u043e \u043e\u0431\u044a\u0435\u043a\u0442\u0430\u043c \u0432\u0440\u0430\u0433\u0430 \u0432 \u0425\u0430\u0440\u044c\u043a\u043e\u0432\u0435. \u0420\u0430\u043d\u043d\u0438\u043c \u0443\u0442\u0440\u043e\u043c \u0431\u044b\u043b \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0435\u043d \u0441\u043a\u043b\u0430\u0434 \u0412\u0421\u0423 \u0441 \u043f\u043e\u0441\u043b\u0435\u0434\u0443\u044e\u0449\u0438\u043c \u0441\u0438\u043b\u044c\u043d\u044b\u043c \u043f\u043e\u0436\u0430\u0440\u043e\u043c, \u0430 \u0434\u043d\u0435\u043c \u0431\u044b\u043b \u0441\u0442\u0435\u0440\u0442 \u0441 \u043b\u0438\u0446\u0430 \u0437\u0435\u043c\u043b\u0438 \u043f\u0440\u043e\u043c\u044b\u0448\u043b\u0435\u043d\u043d\u044b\u0439 \u043e\u0431\u044a\u0435\u043a\u0442 \u0432 \u0418\u043d\u0434\u0443\u0441\u0442\u0440\u0438\u0430\u043b\u044c\u043d\u043e\u043c \u0440\u0430\u0439\u043e\u043d\u0435 \u0433\u043e\u0440\u043e\u0434\u0430.", "7": "<b>Total Posts:</b> 72<br><b>Date:</b> 2024-05-04 16:03:27+00:00<br><b>Author:</b> epoddubny<br><b>Link:</b> https://t.me/s/epoddubny/19802<br><b>Subscribers:</b> 726028<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u041f\u0440\u043e\u0442\u0438\u0432\u043d\u0438\u043a \u043b\u0438\u0448\u0438\u043b\u0441\u044f \u0435\u0449\u0451 \u043e\u0434\u043d\u043e\u0433\u043e \"\u0410\u0431\u0440\u0430\u043c\u0441\u0430\" \u0438 \u043e\u0434\u043d\u043e\u0439 \u0411\u041c\u041f \"\u0411\u0440\u044d\u0434\u043b\u0438\" \u043d\u0430 \u0410\u0432\u0434\u0435\u0435\u0432\u0441\u043a\u043e\u043c \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438. \u041f\u043e \u0431\u043e\u0435\u0432\u044b\u043c \u043c\u0430\u0448\u0438\u043d\u0430\u043c \u0412\u0421\u0423 \u043e\u0442\u0440\u0430\u0431\u043e\u0442\u0430\u043b\u0438 \u043e\u043f\u0435\u0440\u0430\u0442\u043e\u0440\u044b FPV-\u0434\u0440\u043e\u043d\u043e\u0432 \u0438 \u0430\u0440\u0442\u0438\u043b\u043b\u0435\u0440\u0438\u0441\u0442\u044b \u0433\u0440\u0443\u043f\u043f\u0438\u0440\u043e\u0432\u043a\u0438 \u0432\u043e\u0439\u0441\u043a \"\u0426\u0435\u043d\u0442\u0440\". \u0410\u043c\u0435\u0440\u0438\u043a\u0430\u043d\u0441\u043a\u0438\u0439 \u0442\u0430\u043d\u043a \u0431\u044b\u043b \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0435\u043d \u0432\u044b\u0441\u043e\u043a\u043e\u0442\u043e\u0447\u043d\u044b\u043c \u0430\u0440\u0442\u0438\u043b\u043b\u0435\u0440\u0438\u0439\u0441\u043a\u0438\u043c \u0431\u043e\u0435\u043f\u0440\u0438\u043f\u0430\u0441\u043e\u043c \"\u041a\u0440\u0430\u0441\u043d\u043e\u043f\u043e\u043b\u044c\".\u0412\u0438\u0434\u0435\u043e: \u041c\u0438\u043d\u043e\u0431\u043e\u0440\u043e\u043d\u044b \u0420\u0424@epoddubny", "8": "<b>Total Posts:</b> 51<br><b>Date:</b> 2024-05-04 09:33:01+00:00<br><b>Author:</b> rvvoenkor<br><b>Link:</b> https://t.me/s/RVvoenkor/67390<br><b>Subscribers:</b> 1440943<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u203c\ufe0f\ud83c\uddfa\ud83c\udde6\ud83c\uddfa\ud83c\uddf8\u041f\u043e\u043c\u043e\u0449\u044c \u0421\u0428\u0410 \u043f\u043e\u043c\u043e\u0436\u0435\u0442 \u0423\u043a\u0440\u0430\u0438\u043d\u0435 \u0443\u0434\u0435\u0440\u0436\u0430\u0442\u044c \u0444\u0440\u043e\u043d\u0442, \u043d\u043e \u0441\u0438\u0442\u0443\u0430\u0446\u0438\u044f \"\u043e\u0447\u0435\u043d\u044c \u0442\u044f\u0436\u0435\u043b\u0430\u044f\".\u00a0\u25aa\ufe0f\u041e\u0431 \u044d\u0442\u043e\u043c Euronews \u0437\u0430\u044f\u0432\u0438\u043b\u00a0\u0441\u0442\u0430\u0440\u0448\u0438\u0439 \u043d\u0430\u0443\u0447\u043d\u044b\u0439 \u0441\u043e\u0442\u0440\u0443\u0434\u043d\u0438\u043a \u041a\u043e\u0440\u043e\u043b\u0435\u0432\u0441\u043a\u043e\u0433\u043e \u043e\u0431\u044a\u0435\u0434\u0438\u043d\u0435\u043d\u043d\u043e\u0433\u043e \u0438\u043d\u0441\u0442\u0438\u0442\u0443\u0442\u0430 \u043e\u0431\u043e\u0440\u043e\u043d\u043d\u044b\u0445 \u0438\u0441\u0441\u043b\u0435\u0434\u043e\u0432\u0430\u043d\u0438\u0439 RUSI \u042d\u0434 \u0410\u0440\u043d\u043e\u043b\u044c\u0434.\u25aa\ufe0f\"\u041f\u0443\u0442\u0438\u043d, \u0432\u0438\u0434\u0438\u043c\u043e, \u043d\u0430\u0445\u043e\u0434\u0438\u0442\u0441\u044f \u0432 \u0431\u043e\u043b\u0435\u0435 \u0432\u044b\u0438\u0433\u0440\u044b\u0448\u043d\u043e\u043c \u043f\u043e\u043b\u043e\u0436\u0435\u043d\u0438\u0438, \u0447\u0435\u043c 6 \u043c\u0435\u0441\u044f\u0446\u0435\u0432 \u043d\u0430\u0437\u0430\u0434. \u0422\u0430\u043a \u0447\u0442\u043e \u044d\u0442\u043e \u0440\u0430\u0431\u043e\u0442\u0430\u0435\u0442, \u0438 \u043e\u043d \u043c\u043e\u0436\u0435\u0442 \u0438\u0434\u0442\u0438 \u0432 \u043d\u0430\u0441\u0442\u0443\u043f\u043b\u0435\u043d\u0438\u0435. \u0421\u0438\u0442\u0443\u0430\u0446\u0438\u044f \u0434\u043b\u044f \u0443\u043a\u0440\u0430\u0438\u043d\u0446\u0435\u0432 \u0441\u0435\u0439\u0447\u0430\u0441, \u0434\u0435\u0439\u0441\u0442\u0432\u0438\u0442\u0435\u043b\u044c\u043d\u043e, \u043e\u0447\u0435\u043d\u044c \u0442\u044f\u0436\u0435\u043b\u0430\u044f. \u0420\u0435\u0430\u043b\u044c\u043d\u0430\u044f \u0441\u043b\u043e\u0436\u043d\u043e\u0441\u0442\u044c \u0432 \u0442\u043e\u043c, \u0447\u0442\u043e \u0432\u0441\u044f \u0442\u0435\u0445\u043d\u0438\u043a\u0430 \u0438 \u043d\u043e\u0432\u044b\u0435 \u0431\u043e\u0435\u043f\u0440\u0438\u043f\u0430\u0441\u044b \u043f\u043e\u0437\u0432\u043e\u043b\u044f\u0442 \u043b\u0438\u0448\u044c \u0443\u0434\u0435\u0440\u0436\u0430\u0442\u044c \u0444\u0440\u043e\u043d\u0442 \u043d\u0430 \u043c\u0435\u0441\u0442\u0435\",\u00a0- \u0441\u0447\u0438\u0442\u0430\u0435\u0442 \u0410\u0440\u043d\u043e\u043b\u044c\u0434.\u25aa\ufe0f\u0423\u043a\u0440\u0430\u0438\u043d\u0441\u043a\u0438\u0435 \u0432\u043e\u0435\u043d\u043d\u044b\u0435 \u0436\u0430\u043b\u0443\u044e\u0442\u0441\u044f \u043d\u0430 \u043d\u0435\u0445\u0432\u0430\u0442\u043a\u0443 \u043b\u044e\u0434\u0435\u0439.\u00a0\u2796\"\u0421\u043b\u0438\u0448\u043a\u043e\u043c \u043c\u043d\u043e\u0433\u043e \u043b\u044e\u0434\u0435\u0439 \u0443\u0435\u0437\u0436\u0430\u0435\u0442. \u041d\u0435\u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u0438\u0437 \u043d\u0438\u0445 \u043d\u0435 \u0445\u043e\u0442\u044f\u0442 \u0432\u043e\u0435\u0432\u0430\u0442\u044c, \u043d\u0435\u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u043d\u0435 \u043c\u043e\u0433\u0443\u0442 \u0432\u043e\u0435\u0432\u0430\u0442\u044c. \u0418 \u0435\u0441\u043b\u0438 \u043c\u044b \u043f\u043e\u0442\u0435\u0440\u044f\u0435\u043c \u0441\u043b\u0438\u0448\u043a\u043e\u043c \u043c\u043d\u043e\u0433\u043e \u043b\u044e\u0434\u0435\u0439, \u043c\u044b \u043f\u0440\u043e\u0441\u0442\u043e \u043d\u0435 \u0441\u043c\u043e\u0436\u0435\u043c \u0437\u0430\u0449\u0438\u0442\u0438\u0442\u044c \u043d\u0430\u0448\u0443 \u0441\u0442\u0440\u0430\u043d\u0443. \u041f\u043e\u044d\u0442\u043e\u043c\u0443 \u043d\u0430\u043c \u043d\u0443\u0436\u043d\u0430 \u043f\u043e\u043c\u043e\u0449\u044c\",\u00a0- \u0437\u0430\u044f\u0432\u0438\u043b \u0432\u043e\u0435\u043d\u043d\u044b\u0439\u00a0\u0412\u0421\u0423 \u0410\u043b\u0435\u043a\u0441\u0430\u043d\u0434\u0440 \u041c\u0430\u0442\u044f\u0448.\u00a0t.me/RVvoenkor", "9": "<b>Total Posts:</b> 18<br><b>Date:</b> 2024-05-04 04:22:55+00:00<br><b>Author:</b> ukraina_ru<br><b>Link:</b> https://t.me/s/ukraina_ru/198871<br><b>Subscribers:</b> 411999<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u26a1 \u0420\u043e\u0441\u0441\u0438\u0439\u0441\u043a\u0438\u0435 \u0441\u0438\u0441\u0442\u0435\u043c\u044b \u041f\u0412\u041e \u0441\u0431\u0438\u043b\u0438 \u043d\u0430\u0434 \u041a\u0440\u044b\u043c\u043e\u043c \u0447\u0435\u0442\u044b\u0440\u0435 \u0440\u0430\u043a\u0435\u0442\u044b ATACMS, \u043a\u043e\u0442\u043e\u0440\u044b\u0435 \u0437\u0430\u043f\u0443\u0441\u0442\u0438\u043b\u0438 \u0412\u0421\u0423, \u0441\u043e\u043e\u0431\u0449\u0438\u043b\u0438 \u0432 \u041c\u0438\u043d\u043e\u0431\u043e\u0440\u043e\u043d\u044b", "10": "<b>Total Posts:</b> 21<br><b>Date:</b> 2024-05-04 10:46:14+00:00<br><b>Author:</b> slavaded1337<br><b>Link:</b> https://t.me/s/slavaded1337/48376<br><b>Subscribers:</b> 493090<br><b>Text:</b> \u0422\u0435\u043a\u0441\u0442: \u041a\u0430\u0434\u0440\u044b \u0443\u043d\u0438\u0447\u0442\u043e\u0436\u0435\u043d\u0438\u044f \u0430\u043c\u0435\u0440\u0438\u043a\u0430\u043d\u0441\u043a\u043e\u0439 \u0442\u0435\u0445\u043d\u0438\u043a\u0438 \u043d\u0430 \u0410\u0432\u0434\u0435\u0435\u0432\u0441\u043a\u043e\u043c \u043d\u0430\u043f\u0440\u0430\u0432\u043b\u0435\u043d\u0438\u0438.\u0418\u0437\u0432\u0435\u0441\u0442\u043d\u043e, \u0447\u0442\u043e \u0443\u0434\u0430\u043b\u043e\u0441\u044c \u043f\u043e\u0434\u0431\u0438\u0442\u044c \u0410\u0431\u0440\u0430\u043c\u0441 \u0438 \u0411\u0440\u044d\u0434\u043b\u0438.\u0414\u044f\u0434\u044f \u0421\u043b\u0430\u0432\u0430. \u041f\u043e\u0434\u043f\u0438\u0441\u0430\u0442\u044c\u0441\u044f."};

    function displayClusterText() {
        var selectedLabel = document.getElementById("clusterSelector").value;
        var details = clusterDetails[selectedLabel];
        var textDiv = document.getElementById("clusterTextDisplay");
        textDiv.innerHTML = '<p>' + details + '</p>';
        textDiv.classList.remove('hidden');
    }
</script>
