# Backreferences

[slide hideTitle]
#Backreferences se potrivesc cu grupurile anterioare

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Object-And-Classes/04.Java-Fundamentals-Regular-Expressions/EN/04.Java-Fundamentals-Regular-Expressions-14-15-Backreferences-Match-Previous-Groups-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

 ** Backreferences ** sunt o modalitate de a repeta un grup de capturare. O backreference  este utilizată în interiorul unei expresii regulate prin inserarea numărului grupului precedat de o singură bară inversă.

[image assetsSrc="regex-example(24).png" /]

În exemplul de mai sus, primul grup `[a-z] +` se potrivește cu una sau mai multe litere mici de câte ori.

Al doilea grup `[0-9] +` se potrivește cu una sau mai multe cifre.

După aceea, `\ 1` reaplică același„ șir de corespondență ”care va fi capturat de grupul 1 (** [a-z] + **) în timpul rulării.

[/slide]