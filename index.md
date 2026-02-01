---
layout: default
title: Home
hide_title: true
comments: true
weight: 1
---

<script type="text/javascript">
	function getBrowserLanguage() {
	    var language = navigator.language ||   // All browsers
	               (navigator.languages && navigator.languages[0]) || // Chrome / Firefox
	               navigator.userLanguage; // IE <= 10

	    return language;
	}

	function detectLanguage() {
	    var language = getBrowserLanguage();
	    return language.split('-')[0].toLowerCase();
	}

	var userLang = detectLanguage();

	switch (userLang) {
		case 'uk':
			window.location.href = '{{ site.baseurl }}/ua/';
			break;
		case 'ru':
		case 'be':
			window.location.href = '{{ site.baseurl }}/ru/';
			break;
	}

	// Source - https://stackoverflow.com/a/78583202 
	// Posted by EnmanuelGo, modified by community. See post 'Timeline' for change history 
	// Retrieved 2026-01-18, License - CC BY-SA 4.0 
 
	// document.addEventListener("DOMContentLoaded", function() {
	//   const disqus = document.getElementById('disqus_thread');

	//   const observer = new MutationObserver(function(mutations) {
	//     mutations.forEach(function(mutation) {
	//       const iframes = disqus.getElementsByTagName('iframe');
	//       if (iframes.length > 1) {
	//         const commentsIframe = iframes[1];
	//         while (disqus.firstChild) {
	//           disqus.removeChild(disqus.firstChild);
	//         }
	//         disqus.appendChild(commentsIframe);
	//         observer.disconnect();
	//       }
	//     });
	//   });

	//   observer.observe(disqus, { childList: true, subtree: true });
	// });
</script>

{% include main_en.md %}
