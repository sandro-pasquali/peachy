Use as a jQuery plugin

JS
--

Will get back a map of targeted elements on the page. If that element has its own #id, streams.#id 
will address it. Otherwise, will receive incremental id in map prefixed by "sentiment" (sentiment_1, sentiment_2, ...)

var streams = $(".feelings").sentiment();

streams.sentiment_1
.happy(function(el, data) {
})
.veryhappy(function(data) {
})
.sad(function(data) {
	showMessage($(this), "Can this be made a little less negative?");
})
.verysad(function(data) {
	showMessage($(this), "Wow...who hurt you? Maybe save this for your shrink.");
})
.happier(function(data) {
})
.sadder(function(data) {
})
.changed(function(data) {
});

HTML
----

	<textarea class="feelings" style="width: 300px; height: 200px;"></textarea>
	
	<input> works nicely too.

