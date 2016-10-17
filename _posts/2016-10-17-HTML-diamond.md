---
layout: post
title: HTML makes diamond graph
---

Draw diamond

```HTML
<!DOCTYPE html>
<html lang="ko">
<head>
	<meta charset="utf-8" />
	<title>이석원 5238870</title>
</head>
<body>
	<table border = "1" width="350" height="50">
	<?
		$cnt=1;
		for($y=0;$y<=6;$y++){
			for($x=0;$x<=6;$x++){
				$a[$y][$x]=$cnt++;				
				if(($y+$x<=2)||($y+$x>=10)||(($y<$x)&&($x-$y<=6)&&($x-$y>=4))||(($y>$x)&&
					($y-$x>=4)&&($y-$x<=6)))
					$a[$y][$x]=0;

			}
		}
		//출력
		for($y=0;$y<=6;$y++){
			echo "<tr height=40>";
			for($x=0;$x<=6;$x++){
				echo "<td width=40 align=center>";
				if($a[$y][$x] != 0) echo $a[$y][$x];
				else echo "&nbsp;";

				echo "</td>";
			}
			echo "</tr>";
		}
	?>
	</table>
</body>
</html>
```
