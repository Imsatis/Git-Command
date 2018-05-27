Git Cheat Sheet - Git-Flow [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
===============
<hr>
<p align="center">
	<img alt="Git" src="../Img/git-logo.png" height="190" width="455">
</p>
<hr>

# Other Available Languages:
1. [Arabic Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-ar.md)
2. [Chinese Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-zh.md)
3. [Hindi Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-hi.md)
4. [Turkish Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-tr.md)
5. [Spanish Git Cheat Sheet](https://github.com/arslanbilal/git-cheat-sheet/blob/master/other-sheets/git-cheat-sheet-es.md)
6. [Nepalese Git Cheat Sheet](empty)

Git cheat sheet saves you from learning all the commands by heart.

Be free to contribute, update the grammar mistakes. You are also free to add your language file.
<hr>

Git Cheat Sheet Nepalese
===============
###अनुक्रमणिका
* [सेटअप](#सेटअप-)
* [कन्फिगरेसन फाइलहरू](कन्फिगरेसन-फाइलहरू) 
* [सिर्जना](#सिर्जना)
* [स्थानीय परिवर्तनहरू](#स्थानीय-परिवर्तनहरू)
* [खोजी गर्नुहोस्](#खोजी-गर्नुहोस्)
* [कमिटि इतिहास](#कमिटि-इतिहास)
* [शाखाहरू र ट्यागहरू](#शाखाहरू-र-ट्यागहरू)
* [अपडेट र प्रकाशित](#अपडेट-र-प्रकाशित)
* [मर्ज र विस्थापन](#मर्ज-र-विस्थापन)
* [पूर्ववत](#पूर्ववत)
* [Git प्रवाह](#Git-प्रवाह)

<hr>
###सेटअप                                                                  गर्न
 को लागी


#####वर्तमान कन्फिगरेसन देखनुहोस्:
```
git config --list
```

#####भण्डार कन्फिगरेसन देखनुहोस््:
```
git config --local --list
```

#####विश्वव्यापी विन्यास देखनुहोस्:
```
git config --global --list
```

#####प्रणाली कन्फिगरेसन देखनुहोस््:
```
git config --system --list
```

#####संस्करण इतिहास पूर्वावलोकन गर्दा क्रेडिटको लागि पहिचान योग्य नाम सेट गर्न:
```
git config --global user.name “[firstname lastname]”
```

#####एक इमेल ठेगाना सेट गर्न जुन हरेक इतिहास मार्करसँग सम्बन्धित हुनेछ:
```
git config --global user.email “[valid-email]”
```

#####सजिलो समीक्षाको लागि Git को लागि स्वचालित आदेश रेखा रंग सेट गर्न:
```
git config --global color.ui auto
```

#####प्रतिबद्धताको लागि वैश्विक सम्पादक सेट गर्न:
```
git config --global core.editor vi
```

<hr>
##कन्फिगरेसन फाइलहरू

#####भण्डार विशिष्ट कन्फिगरेसन फाइल [--local]:
```
<repo>/.git/config
```

#####प्रयोगकर्ता-विशिष्ट कन्फिगरेसन फाइल [--global]:
```
~/.gitconfig
```

#####प्रणाली-विस्तृत विन्यास फाइल [--system]:
```
/etc/gitconfig
```

<hr>
##सिर्जना 

#####अवस्थित भण्डार क्लोन गर्न:

त्यहाँ दुई तरिकाहरू छन्:

को द्वारा SSH

```
git clone ssh://user@domain.com/repo.git
```

को द्वारा HTTP

```
git clone http://domain.com/user/repo.git
```

#####नयाँ स्थानीय भण्डार सिर्जना गर्न:
```
git init
```






































