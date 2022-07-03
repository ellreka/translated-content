---
title: 'HTMLMediaElement: timeupdate イベント'
slug: Web/API/HTMLMediaElement/timeupdate_event
tags:
  - Audio
  - Event
  - HTMLMediaElement
  - Reference
  - Video
  - Web
  - timeupdate
translation_of: Web/API/HTMLMediaElement/timeupdate_event
---
{{APIRef("HTMLMediaElement")}}

<span class="seoSummary">`timeupdate` イベントは、`currentTime` 属性で示される時刻が更新されたときに発生します。</span>

イベントの頻度はシステムの負荷に依存しますが、およそ 4Hz と 66Hz との間でスローされます (イベントハンドラーが実行するのに 250 ms 以上かかることはないと仮定します)。ユーザーエージェントはシステム負荷とその都度イベントを処理する平均コストに基づいて、イベントの頻度を変えることが推奨されているため、ユーザーエージェントがビデオのデコード中に快適に処理できるよりも頻繁に UI 更新が行われることはありません。

<table class="properties">
 <tbody>
  <tr>
   <th scope="row">バブリング</th>
   <td>なし</td>
  </tr>
  <tr>
   <th scope="row">キャンセル可能</th>
   <td>不可</td>
  </tr>
  <tr>
   <th scope="row">インターフェイス</th>
   <td>{{DOMxRef("Event")}}</td>
  </tr>
  <tr>
   <th scope="row">対象</th>
   <td>Element</td>
  </tr>
  <tr>
   <th scope="row">既定のアクション</th>
   <td>なし</td>
  </tr>
  <tr>
   <th scope="row">イベントハンドラープロパティ</th>
   <td>{{domxref("GlobalEventHandlers.ontimeupdate")}}</td>
  </tr>
  <tr>
   <th scope="row">仕様書</th>
   <td><a class="external" href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-playing">HTML5 media</a></td>
  </tr>
 </tbody>
</table>

<h2 id="Examples" name="Examples">例</h2>

これらの例は、 HTMLMediaElement の `timeupdate` イベントのイベントリスナーを追加し、イベントが発生してイベントハンドラーが動作するときにメッセージを投稿します。なお、イベントの頻度はシステムの稼働状況に依存します。

`addEventListener()` の使用:

<pre class="brush: js">const video = document.querySelector('video');

video.addEventListener('timeupdate', (event) =&gt; {
  console.log('The currentTime attribute has been updated. Again.');
});</pre>

`ontimeupdate` イベントハンドラープロパティの使用:

<pre class="brush: js">const video = document.querySelector('video');

video.ontimeupdate = (event) =&gt; {
  console.log('The currentTime attribute has been updated. Again.');
};</pre>

<h2 id="Specifications" name="Specifications">仕様書</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">仕様書</th>
   <th scope="col">状態</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('HTML WHATWG', "media.html#event-media-timeupdate", "timeupdate media event")}}</td>
   <td>{{Spec2('HTML WHATWG')}}</td>
  </tr>
  <tr>
   <td>{{SpecName('HTML5 W3C', "embedded-content-0.html#event-media-timeupdate", "timeupdate media event")}}</td>
   <td>{{Spec2('HTML5 W3C')}}</td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility" name="Browser_compatibility">ブラウザーの互換性</h2>

{{Compat("api.HTMLMediaElement.timeupdate_event")}}

<h2 id="Related_Events" name="Related_Events">関連イベント</h2>

<ul>
 <li>{{domxref("HTMLMediaElement.playing_event", 'HTMLMediaElement: playing イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.waiting_event", 'HTMLMediaElement: waiting イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.seeking_event", 'HTMLMediaElement: seeking イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.seeked_event", 'HTMLMediaElement: seeked イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.ended_event", 'HTMLMediaElement: ended イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.loadedmetadata_event", 'HTMLMediaElement: loadedmetadata イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.loadeddata_event", 'HTMLMediaElement: loadeddata イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.canplay_event", 'HTMLMediaElement: canplay イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.canplaythrough_event", 'HTMLMediaElement: canplaythrough イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.durationchange_event", 'HTMLMediaElement: durationchange イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.timeupdate_event", 'HTMLMediaElement: timeupdate イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.play_event", 'HTMLMediaElement: play イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.pause_event", 'HTMLMediaElement: pause イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.ratechange_event", 'HTMLMediaElement: ratechange イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.volumechange_event", 'HTMLMediaElement: volumechange イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.suspend_event", 'HTMLMediaElement: suspend イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.emptied_event", 'HTMLMediaElement: emptied イベント')}}</li>
 <li>{{domxref("HTMLMediaElement.stalled_event", 'HTMLMediaElement: stalled イベント')}}</li>
</ul>

<h2 id="See_also" name="See_also">関連情報</h2>

<ul>
 <li>{{domxref("HTMLAudioElement")}}</li>
 <li>{{domxref("HTMLVideoElement")}}</li>
 <li>{{HTMLElement("audio")}}</li>
 <li>{{HTMLElement("video")}}</li>
</ul>