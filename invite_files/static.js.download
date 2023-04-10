var renderCanvas = function(){
	var canvas = document.getElementById('invitation-card');
	var ctx = canvas.getContext('2d');
	canvas.width = 1354;
	canvas.height = 1900;
	var background = new Image();
	background.src = biicore.webroot + '/invitation/templates/'+invitationInfo.templateID+'/bg.png';
	background.onload = function(){
		ctx.drawImage(this, 0,0,this.width, this.height);

		ctx.textBaseline = 'middle';
		ctx.textAlign = 'center';
		ctx.fillStyle = '#665044';

		canvas.style.letterSpacing = '10px';
		ctx.font = "100 70px 'Tourney', cursive";
		ctx.fillText('Invitation', canvas.width/2, 230);
		ctx.save();

		canvas.style.letterSpacing = '6px';
		ctx = canvas.getContext('2d');
		ctx.font = "35px 'Jura', cursive";
		ctx.fillText('Save The Date', canvas.width/2, 300);
		ctx.save();

		canvas.style.letterSpacing = '0';
		ctx = canvas.getContext('2d');
		ctx.font = "100px 'dancing_scriptregular', cursive";
		ctx.textBaseline = 'middle';
		ctx.textAlign = 'center';
		ctx.fillText(invitationInfo.groom_name_short + '  &  ' + invitationInfo.bride_name_short, canvas.width/2, 590);
		ctx.save();

		canvas.style.letterSpacing = '2px';
		ctx.font = "45px 'Jura', cursive";
		ctx.fillText('TRÂN TRỌNG KÍNH MỜI', canvas.width/2, 730);
		ctx.save();

		ctx.font = "bold 60px 'comfortaaregular', cursive";
		ctx.fillText(invitationInfo.guest_name, canvas.width/2, 840);
		ctx.save();

		const canvasTxt0 = window.canvasTxt.default;
		canvasTxt0.font = "'Jura', cursive";
		canvasTxt0.fontSize = 45;
		canvasTxt0.fontWeight = '200';
		canvasTxt0.vAlign = 'top';
		canvasTxt0.align = 'center';
		canvasTxt0.lineHeight = 55;
		canvasTxt0.drawText(ctx, 'Đến dự buổi tiệc chung vui cùng gia đình chúng tôi tại', 120, 900, canvas.width-220, 200);
		ctx.save();

		const canvasTxt = window.canvasTxt.default;
		canvasTxt.font = "'comfortaaregular', cursive";
		canvasTxt.fontSize = 40;
		canvasTxt.fontWeight = 'bold';
		canvasTxt.vAlign = 'top';
		canvasTxt.align = 'center';
		canvasTxt.lineHeight = 60;
		canvasTxt.drawText(ctx, invitationInfo.event_address, 110, 1050, canvas.width-220, 200);
		ctx.save();

		ctx.font = "bold 45px 'comfortaaregular', cursive";
		ctx.fillText(('Vào lúc ' + invitationInfo.event_time).toUpperCase(), canvas.width/2, 1270);
		ctx.save();
		
		ctx.font = "bold 45px 'comfortaaregular', cursive";
		ctx.fillText(invitationInfo.event_date.toUpperCase(), canvas.width/2, 1350);
		ctx.save();

		const canvasTxt1 = window.canvasTxt.default;
		canvasTxt1.font = "'dancing_scriptregular', cursive";
		canvasTxt1.fontSize = 50;
		canvasTxt1.fontWeight = '200';
		canvasTxt1.vAlign = 'top';
		canvasTxt1.align = 'center';
		canvasTxt1.lineHeight = 60;
		canvasTxt1.drawText(ctx, 'Sự hiện diện của quý khách là niềm vinh hạnh cho gia đình chúng tôi!', 220, 1430, canvas.width-420, 200);
		ctx.save();
	};
}
window.addEventListener('load', function(){
	WebFont.load({
		custom: {
			families: ['dancing_scriptregular', 'comfortaaregular']
		},
		google: {families: ['Jura', 'Great Vibes', 'Tourney:100']},
		active: function(){
			renderCanvas();
			let renderCount = 0;
			const intID = setInterval(function(){
				renderCanvas();
				if(renderCount >= 3) clearInterval(intID);
				renderCount++;
			},100);
		}
	});
});