# ymetrica
Цели яндекс метрики

1. цель на sabmit вешается на тег form
onSubmit="ym('XXXXXX','reachGoal', 'TARGET_NAME');"

2. цель на click 
onclick="ym(XXXXXX, 'reachGoal', 'opt_form_first_screen_sent'); return true;"


3. Цель на меню. Считает пункты меню, добавляет к ним классы и по клику отрабатывает цель

<code>
	var i = 0;
	var menuli = $('.nav__sub li');
	$.each(menuli, function (index, value) {
		i++;
		$(value).addClass("metric"+i);	
	});
	$('metric1').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_1_button'); return true;
	});	
	$('metric2').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_2_button'); return true;
	});
	$('metric3').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_3_button'); return true;
	});
	$('metric4').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_4_button'); return true;
	});
	$('metric5').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_5_button'); return true;
	});
	$('metric6').on( "click", function() {
	  ym(XXXXXXXX, 'reachGoal', '2_menu_6_button'); return true;
	});

</code>
