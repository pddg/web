+++
title = "Contact"
weight = 30
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/pudding@mail.poyo.info">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="氏名"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="メールアドレス">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="4" placeholder="メッセージ"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="メッセージを送信" class="special" /></li>
		<li><input type="reset" value="リセット" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Message arrived" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">メッセージありがとうございます．</span>

<script>
$(document).ready(function($) { 
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>


{{< socialLinks >}}
