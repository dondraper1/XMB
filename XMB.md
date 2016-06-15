# XMB
XMB Rainmeter Skin 


[Rainmeter]
Update=1000
Author=DonDraper1

[Metadata]
Name=XMB
Version=1.0
License=Creative Commons Attribution-Non-Commercial-Share Alike 3.0
Information=PS3's XMB now available on your PC!

[Variables]

Path1=::{21EC2020-3AEA-1069-A2DD-08002b30309d}
Path1Name=Control Panel
Path2="C:\Users\%username%\Documents"
Path2Name=Documents
Path3="::{20D04FE0-3AEA-1069-A2D8-08002B30309D}"
Path3Name=Explorer
Path4="C:\Users\%username%\Pictures"
Path4Name=Images
Path5="C:\Users\%username%\Music"
Path5Name=Music
Path6="C:\Users\%username%\Videos"
Path6Name=Video
Path7=https://www.facebook.com
Path7Name=Facebook

App1="C:\Program Files (x86)\iTunes\iTunes.exe"
App1Name=iTunes
App2="%windir%\ehome\ehshell.exe"
App2Name=Media Center
App3="C:\Program Files (x86)\Diablo III\Diablo III Launcher.exe"
App3Name=Diablo III
App4="C:\Program Files (x86)\Steam\Steam.exe"
App4Name=Steam
App5="C:\Program Files\Internet Explorer\iexplore.exe"
App5Name=Internet Explorer
App6="C:\Program Files (x86)\Adobe\Adobe Photoshop CS5\Photoshop.exe"
App6Name=Photoshop

SolidColor=0,0,0,1

font=Existence Light
color=255,255,255,200

;MEASURES

[mSSID]
Measure=Plugin
Plugin=WiFiStatus
WiFiInfoType=SSID
WiFiIntfID=0

;METERS

[BGSet1]
Meter=STRING
X=25
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "CP"][!RainmeterShowMeter "CPText"][!RainmeterShowMeter "Documents" ][!RainmeterShowMeter "DocumentsText"][!RainmeterShowMeter "Explorer"][!RainmeterShowMeter "ExplorerText"][!RainmeterRedraw]

[BGSet2]
Meter=String
X=25
Y=5
SolidColor=#SolidColor#
H=320
W=65
MouseLeaveAction=!Execute[!RainmeterHideMeter "CP"][!RainmeterHideMeter "CPText"][!RainmeterHideMeter "Documents" ][!RainmeterHideMeter "DocumentsText"][!RainmeterHideMeter "Explorer"][!RainmeterHideMeter "ExplorerText"][!RainmeterRedraw]


[SettingsImage]
Meter=IMAGE
ImageName=Settings.png
X=25
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "SettingsText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "SettingsText"][!RainmeterRedraw]

[SettingsText]
Meter=STRING
x=-5r
Y=50r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Settings"
Hidden=1

[CP]
Meter=IMAGE
ImageName=cp.png
X=r
Y=75r
SolidColor=0,0,0,1
H=60
W=60
Hidden=1
LeftMouseDownAction=!Execute["#Path1#"]

[CPText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#Path1Name#"
LeftMouseDownAction=!Execute["#Path1#"]
Hidden=1

[Documents]
Meter=Image
ImageName=Docs.png
X=25
Y=50r
SolidColor=0,0,0,1
H=60
W=60
LeftMouseDownAction=!Execute["#Path2#"]
Hidden=1

[DocumentsText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#Path2Name#"
LeftMouseDownAction=!Execute["#Path2#"]
Hidden=1

[Explorer]
Meter=Image
ImageName=explorer.ico
X=25
Y=50r
H=60
W=60
Hidden=1
LeftMouseDownAction=!Execute["#Path3#"]

[ExplorerText]
Meter=String
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#Path3Name#"
LeftMouseDownAction=!Execute["#Path3#"]
Hidden=1

[BGPhoto1]
Meter=STRING
X=50r
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "PhotoLib"][!RainmeterShowMeter "PhotoLibText"][!RainmeterShowMeter "CS5" ][!RainmeterShowMeter "CS5Text"][!RainmeterRedraw]

[BGPhoto2]
Meter=String
X=r
Y=5
SolidColor=#SolidColor#
H=300
W=150
MouseLeaveAction=!Execute[!RainmeterHideMeter "PhotoLib"][!RainmeterHideMeter "PhotoLibText"][!RainmeterHideMeter "CS5" ][!RainmeterHideMeter "CS5Text"]s[!RainmeterRedraw]


[Photo]
Meter=IMAGE
ImageName=photo.png
X=r
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "PhotoText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "PhotoText"][!RainmeterRedraw]

[PhotoText]
Meter=STRING
x=-2r
Y=50r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Photos"
Hidden=1
LeftMouseDownAction=!Execute ["#Path4#"]

[PhotoLib]
Meter=IMAGE
ImageName=Docs.png
X=-7r
Y=75r
H=60
W=60
LeftMouseDownAction=!Execute["#App4#"]
Hidden=1

[PhotoLibText]
Meter=STRING
x=55r
Y=20r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
LeftMouseDownAction=!Execute["#App4#"]
Text="Photo Library"
Hidden=1

[CS5]
Meter=IMAGE
ImageName=CS5.png
X=-55r
Y=75r
H=60
W=60
LeftMouseDownAction=!Execute["#App6#"]
Hidden=1

[CS5Text]
Meter=STRING
x=50r
Y=20r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
LeftMouseDownAction=!Execute["#App6#"]
Text="Photoshop"
Hidden=1

[BGMusic1]
Meter=STRING
X=50r
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "Library"][!RainmeterShowMeter "LibraryText"][!RainmeterShowMeter "iTunes" ][!RainmeterShowMeter "iTunesText"][!RainmeterRedraw]

[BGMusic2]
Meter=String
X=r
Y=5
SolidColor=#SolidColor#
H=300
W=150
MouseLeaveAction=!Execute[!RainmeterHideMeter "Library"][!RainmeterHideMeter "LibraryText"][!RainmeterHideMeter "iTunes" ][!RainmeterHideMeter "iTunesText"][!RainmeterRedraw]


[Music]
Meter=IMAGE
ImageName=Music.png
X=r
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "MusicText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "MusicText"][!RainmeterRedraw]

[MusicText]
Meter=STRING
x=5r
Y=50r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Music"
Hidden=1

[Library]
Meter=IMAGE
ImageName=Docs.png
X=-7r
Y=75r
H=60
W=60
LeftMouseDownAction=!Execute["#Path5#"]
Hidden=1

[LibraryText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Library"
LeftMouseDownAction=!Execute["#Path5#"]
Hidden=1

[iTunes]
Meter=IMAGE
ImageName=iTunes.png
X=-55r
Y=50r
H=60
W=60
LeftMouseDownAction=!Execute["#App1#"]
Hidden=1

[iTunesText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#App1Name#"
LeftMouseDownAction=!Execute["#App1#"]
Hidden=1


[BGMovies1]
Meter=STRING
X=50r
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "Video"][!RainmeterShowMeter "VideoText"][!RainmeterShowMeter "WMP" ][!RainmeterShowMeter "WMPText"][!RainmeterRedraw]

[BGMovies2]
Meter=String
X=r
Y=5
SolidColor=#SolidColor#
H=300
W=150
MouseLeaveAction=!Execute[!RainmeterHideMeter "Video"][!RainmeterHideMeter "VideoText"][!RainmeterHideMeter "WMP" ][!RainmeterHideMeter "WMPText"][!RainmeterRedraw]

[Movies]
Meter=IMAGE
ImageName=movie.png
X=r
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "MovieText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "MovieText"][!RainmeterRedraw]

[MovieText]
Meter=STRING
x=r
Y=50r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Movies"
Hidden=1

[Video]
Meter=IMAGE
ImageName=Docs.png
X=-7r
Y=75r
H=60
W=60
LeftMouseDownAction=!Execute["#Path6#"]
Hidden=1

[VideoText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Videos"
LeftMouseDownAction=!Execute["#Path6#"]
Hidden=1

[WMP]
Meter=IMAGE
ImageName=WMP.ico
X=-55r
Y=50r
H=60
W=60
LeftMouseDownAction=!Execute["#App2#"]
Hidden=1

[WMPText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Media Center"
LeftMouseDownAction=!Execute["#App2#"]
Hidden=1

[BGGames1]
Meter=STRING
X=50r
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "Steam"][!RainmeterShowMeter "SteamText"][!RainmeterShowMeter "Diablo" ][!RainmeterShowMeter "DiabloText"][!RainmeterRedraw]

[BGGames2]
Meter=String
X=r
Y=5
SolidColor=#SolidColor#
H=300
W=150
MouseLeaveAction=!Execute[!RainmeterHideMeter "Steam"][!RainmeterHideMeter "SteamText"][!RainmeterHideMeter "Diablo" ][!RainmeterHideMeter "DiabloText"][!RainmeterRedraw]


[Games]
Meter=IMAGE
ImageName=game.png
X=r
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "GameText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "GameText"][!RainmeterRedraw]

[GameText]
Meter=STRING
x=3r
Y=50r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Game"
Hidden=1

[Diablo]
Meter=IMAGE
ImageName=Diablo.png
X=-7r
Y=75r
H=60
W=60
LeftMouseDownAction=!Execute["#App3#"]
Hidden=1

[DiabloText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#App3Name#"
LeftMouseDownAction=!Execute["#App3#"]
Hidden=1

[Steam]
Meter=IMAGE
ImageName=steam.ico
X=-55r
Y=50r
H=60
W=60
LeftMouseDownAction=!Execute["#App4#"]
Hidden=1

[SteamText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#App4Name#"
LeftMouseDownAction=!Execute["#App4#"]
Hidden=1

[BGNetwork1]
Meter=STRING
X=50r
Y=5
SolidColor=#SolidColor#
H=60
w=60
LeftMouseDownAction=!Execute[!RainmeterShowMeter "IE"][!RainmeterShowMeter "IEText"][!RainmeterShowMeter "Facebook" ][!RainmeterShowMeter "FacebookText"][!RainmeterShowMeter "WiFi"][!RainmeterShowMeter "WiFiText"][!RainmeterRedraw]

[BGNetwork2]
Meter=String
X=r
Y=5
SolidColor=#SolidColor#
H=300
W=150
MouseLeaveAction=!Execute[!RainmeterHideMeter "IE"][!RainmeterHideMeter "IEText"][!RainmeterHideMeter "Facebook" ][!RainmeterHideMeter "FacebookText"][!RainmeterHideMeter "WiFi"][!RainmeterHideMeter "WiFiText"][!RainmeterRedraw]

[Network]
Meter=IMAGE
ImageName=network.png
X=r
Y=5
SolidColor=0,0,0,1
H=60
W=60
MouseOverAction=!Execute [!RainmeterShowMeter "NetworkText"][!RainmeterRedraw]
MouseLeaveAction=!Execute[!RainmeterHideMeter "NetworkText"][!RainmeterRedraw]


[NetworkText]
Meter=STRING
x=-7r
Y=51r
SolidColor=0,0,0,1
FontFace=#font#
FontSize=15
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="Network"
Hidden=1

[IE]
Meter=IMAGE
ImageName=www.png
X=r
Y=50r
H=60
W=60
LeftMouseDownAction=!Execute["#App5#"]
Hidden=1

[IEText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#App5Name#"
LeftMouseDownAction=!Execute["#App5#"]
Hidden=1

[Facebook]
Meter=IMAGE
ImageName=Facebook.png
X=-55r
Y=50r
H=55
W=65
LeftMouseDownAction=!Execute["#Path7#"]
Hidden=1

[FacebookText]
Meter=STRING
X=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Text="#Path7Name#"
LeftMouseDownAction=!Execute["#Path7#"]
Hidden=1

[WiFi]
Meter=IMAGE
ImageName=wifi.png
X=-55r
Y=50r
H=60
W=60
Hidden=1

[WiFIText]
MeasureName=mSSID
Meter=String
x=55r
Y=20r
FontFace=#font#
FontSize=18
FontColor=#color#
StringStyle=Bold
AntiAlias=1
Hidden=1

