# ymetrica
Цели яндекс метрики

1. цель на sabmit вешается на тег form
<code>onSubmit="ym('XXXXXX','reachGoal', 'TARGET_NAME');"</code>


2. цель на click 

<code>onclick="ym(XXXXXX, 'reachGoal', 'opt_form_first_screen_sent'); return true;"</code>


3. Цель на меню. Считает пункты меню, добавляет к ним классы и по клику отрабатывает цель (jquery)

<code>

	var i = 0;

	var menuli = $('.nav__sub li');

	$.each(menuli, function (index, value) {
		i++;
		$(value).addClass("metric"+i);
	});
	
	$('metric1').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_1_button'); return true;
	});
	$('metric2').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_2_button'); return true;
	});
	$('metric3').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_3_button'); return true;
	});
	$('metric4').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_4_button'); return true;
	});
	$('metric5').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_5_button'); return true;
	});
	$('metric6').on( "click", function() {
	  ym(43176784, 'reachGoal', '2_menu_6_button'); return true;
	});
</code>

4. Цель на заполнение полей. Проверяет заполнены ли поля формы и коректен ли email и отправляет цель (jquery)

<code>

$(document).ready(function(){
   $(document).on('change','.bx-soa-customer input',function(e){
        var tel = $('#soa-property-3').val();
		var email = $('#soa-property-2').val();
		var adress = $('#soa-property-7').val();
		if((tel != "") && (email != "") && (adress != "")){

			var re_email = /^([A-Za-z0-9_\-\.])+\@([A-Za-z0-9_\-\.])+\.([A-Za-z]{2,4})$/;
			
			if(re_email.test(email) != false) {
				console.log("ок");
				ym(43176784, 'reachGoal', 'completed_form'); return true;
			}
		}
		
      e.preventDefault();
   });
});
</code>
