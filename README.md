# sometime-ago
PHP function that takes your unix epoch and converts it to sometime ago - e.g 3 seconds ago, 3 years ago

//get hw many times ago
function timecalc($time) {
	$sdiff=date('U')-$time;
	if($sdiff<60){ if(floor($sdiff)>1){$sss="s";} else {$sss="";} $time=floor($sdiff)." Second".$sss." ago";}
	 $mdiff=floor($sdiff/60);
	if($mdiff<60 && $mdiff>0){if(floor($mdiff)>1){$sss="s";} else {$sss="";} $time=floor($mdiff)." Min".$sss." ago";}
	 $hdiff=floor($mdiff/60);
	if($hdiff<24 && $hdiff>0){if(floor($hdiff)>1){$sss="s";} else {$sss="";} $time=floor($hdiff)." Hr".$sss." ago";}
	 $ddiff=floor($hdiff/24);
	if($ddiff<28 && $ddiff>0){if(floor($ddiff)>1){$sss="s";} else {$sss="";} $time=floor($ddiff)." Day".$sss." ago";}
	 $modiff=floor($ddiff/28);
	if($modiff<13 && $modiff>0){if(floor($modiff)>1){$sss="s";} else {$sss="";} $time=floor($modiff)." Month".$sss." ago";}
	 $ydiff=floor($modiff/13);
	if($ydiff>=1){if(floor($ydiff)>1){$sss="s";} else {$sss="";} $time=floor($ydiff)." Year".$sss." ago";}
	return $time;}
