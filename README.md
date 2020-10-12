# mohamed
<html>
  <head>
    <link href="https://fonts.googleapis.com/css?family=Roboto:300,400,900" rel="stylesheet" type="text/css">
    <link href="https://fonts.googleapis.com/css?family=VT323" rel="stylesheet">
    <script src="https://picturelements.github.io/PeOS/console_load.js"></script>
    <script src="https://picturelements.github.io/PeOS/console.js"></script>
    <link href="https://picturelements.github.io/PeOS/console.css" rel="stylesheet" type="text/css">
  </head>
  <body oncontextmenu="return contextShow">
    <audio id="taskbahSound" loop preload="auto">
      <source src="https://picturelements.github.io/images/win_icons/LockIt.mp3">
    </audio>
    <button id="gofull" style="display:none; position:fixed; z-index:100;">GO FULLSCREEN</button>
    <div id="desktopwrapper" class="grad backOverride">
      <div id="desktop">
        <div id="test"></div>
        <div id="selectbox"></div>
        <div id="shadow"></div>
      </div>
    </div>
    <div id="context">
      <div class="contextitem">Open</div>
      <div class="contextitem">Open All</div>
      <div class="contextitem">Rename</div>
      <div class="contextitem">Pin to taskbar</div>
      <div class="contextitem">Pin</div>
      <!--5-->
      <div class="contextitem">Unpin</div>
      <div class="contextitem">Open new</div>
      <div class="contextitem">Close</div>
      <div class="contextitem">Fullscreen</div>
      <div class="contextitem">Enable context menu</div>
      <!--10-->
      <div class="contextitem">Change wallpaper</div>
      <div class="contextitem tickbox" ticked="false">Lock taskbar</div>
      <div class="contextitem tickbox" ticked="false">Lock the taskbah</div>
      <div class="contextitem">Open</div>
      <div class="contextitem">Go to directory</div>
      <!--15-->
      <div class="contextitem">Open in new explorer</div>
      <div class="contextitem">Open as HTML</div>
    </div>
    <div id="searchbar">
      <div id="searchbarbar" expanded="false">
        <div class="sbbitem" onclick="sbbToggle(this)">
          <div class="sbbicon">
            <svg width="90" height="90" viewBox="0 0 90 90" fill="none">
              <line x1="25" y1="34" x2="65" y2="34" stroke-width="4"></line>
              <line x1="25" y1="45" x2="65" y2="45" stroke-width="4"></line>
              <line x1="25" y1="56" x2="65" y2="56" stroke-width="4"></line>
            </svg>
          </div>
          <div id="sbblabel"><b>SEARCH</b></div>
        </div>
        <div class="sbbitem" onclick="sbbHome()">
          <div class="sbbicon">
            <svg viewBox="0 0 90 90" height="90" width="90">
              <path d="M28 65 L28 37 L45 25 L62 37 L62 65 L50 65 L50 52 L40 52 L40 65 Z" fill="none"></path>
            </svg>
          </div>
          <div id="sbblabel">Home</div>
        </div>
        <div class="sbbitem2" onclick="openSettings()">
          <!--style="background-image:url(https://picturelements.github.io/images/win_icons/cog.png)"-->
          <div class="sbbicon">
            <svg viewBox="0 0 90 90" height="90" width="90">
              <path id="cog" fill="none"></path>
              <circle cx="45" cy="45" r="7" fill="none"></circle>
            </svg>
          </div>
          <div id="sbblabel">Settings</div>
        </div>
        <div class="sbbitem2" onclick="togglePower()" style="display:none">
          <div class="sbbicon">
            <svg viewBox="0 0 90 90" height="90" width="90">
              <path d="M50 30 A18 18 0 1 1 40 30" fill="none"></path>
              <line x1="45" y1="23" x2="45" y2="40"></line>
            </svg>
          </div>
          <div id="sbblabel">Power</div>
        </div>
      </div>
      <div id="powerbar">
        <div class="poweritem">Restart</div>
        <div class="poweritem">Power off</div>
      </div>
      <div id="innerbar"></div>
    </div>
    <div id="clockbar" class="specColor" style="display:none;">
      <p id="clocklbl"></p>
      <table id="calendar">
      </table>
      <div class="clock specColor">
        <svg id="clocksvg" width="100" height="100" viewBox="0 0 100 100">
          <circle cx="50" cy="50" r="47" fill="#eee" stroke="none">
        </circle></svg>
        <div id="hour"></div>
        <div id="minute"></div>
        <div id="second"></div>
        <div id="seconddot"></div>
      </div>
      <p onclick="openSettings()" id="edittime">Edit time and date...</p>
    </div>
    <div id="taskbar" style="bottom: 0vw">
      <div id="home">
        <svg width="105" height="90" viewBox="0 0 105 90">
          <rect x="27.5" y="20" width="50" height="50" fill="none" stroke-width="3"></rect>
          <rect height="43" width="43" y="23.5" x="31" stroke="none"></rect>
          <text x="52.5" y="56" fill="black" stroke="none" text-anchor="middle" style="font-size:2.2em">Pe</text>
        </svg>
      </div>
      <input id="search" placeholder="Search in PeOS" autocomplete="off"></input>
      <div id="infocorner">
        <div id="batterywrapper">
          <div id="battery" charging="true">
            <svg width="160" height="90" viewBox="0 0 160 90">
              <rect x="5" y="5" width="130" height="80" fill="none" stroke="white" stroke-width="10"></rect>
              <rect class="batteryindicator" x="20" y="20" width="100" height="50"></rect>
              <rect x="140" y="30" width="20" height="30"></rect>
            </svg>
          </div>
        </div>
        <div id="wifi" level="2">
          <svg viewBox="0 0 90 90" height="90" width="90">
            <path d="M5 85 A80 80 0 0 1 85 5" fill="none" greyout="012"></path>
            <path d="M25 85 A60 60 0 0 1 85 25" fill="none" greyout="01"></path>
            <path d="M45 85 A40 40 0 0 1 85 45" fill="none" greyout="0"></path>
            <circle cx="75" cy="75" r="10" stroke="none"></circle>
          </svg>
        </div>
        <div id="time" onclick="toggleClock()">22:20<br>2016-10-07</div>
      </div>
    </div>
    <div id="loadscreen"></div>
    <style id="specCols"></style>
  
    <!--HTML buffers-->
    <div id="settingsbuffer" style="display:none">
      <div id="settingscontainer">
        <h>Time and Date</h>
        <p>Time zone:</p>
        <select id="timezone" onchange="updateTime()">
          <option>Local</option>
          <option>Custom offset</option>
        </select>
        <input id="prectz" disabled="true" placeholder="Time offset in minutes" oninput="newTime()"></input>
        <input id="dateset" type="date" oninput="newTime()"></input>
        <p id="tzlbl"></p>
        <br>
        <button onclick="setTime()">Set time</button>
        <h>Filenames</h>
        <p>Reset all filenames to their defaults. This action will take effect immediately and cannot be undone.</p>
        <button onclick="resetNamesRelay()">Reset to default</button>
        <h>System data</h>
        <p>Reset system data. All saved data will be deleted and the system will restart. This action cannot be undone.</p>
        <button onclick="resetAll()">Reset system</button>
        <h>Windows</h>
        <p>Set the default size of opened window. Default is 60x35.<br><br><span id="winW">Window width: 40</span></p>
        <input class="sizeslider" type="range" min="20" max="100" value="40" oninput="updateSize(0)"></input>
        <p id="winH">Window height: 25</p>
        <input class="sizeslider" type="range" min="15" max="80" value="25" oninput="updateSize(1)"></input>
        <h id="backH">Color scheme/Backgrounds</h>
        <p>Color scheme</p>
        <div id="colorbar"></div>
        <br>
        <p>Desktop background</p>
        <div id="backbar"></div>
        <div id="preview" class="grad backOverride"></div>
        <br>
        <br>
      </div>
    </div>
    <div id="resultsbuffer" style="display:none">
      <div id="resultsbar">
        <div id="innerresults">
          <div id="searchmsg">Start typing to browse programs, other programs, or programs.<br><br><pt>Protip: press any arrow key to get all programs.</pt></div>
        </div>
      </div>
    </div>
    <div id="mainbuffer" style="display:none">
      <div id="programbar">
        <div class="pbitem">
          <div id="pbicon"></div>
          <div id="pbtitle"></div>
        </div>
      </div>
      <div id="puzzlebar">
        <div class="puzzle specColor" style="display:none" active></div>
      </div>
    </div>
    <div id="explorerbuffer" style="display:none">
      <div class="filebar">
        <div class="histbtn normCol" active="false">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <path d="M20 45 L55 20 L55 70"></path>
          </svg>
        </div>
        <div class="histbtn normCol" active="false">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <path d="M30 20 L65 45 L30 70"></path>
          </svg>
        </div>
        <input class="path" spellcheck="false">
        <div class="histbtn normCol square" onclick="parseGeneralURL(this,this.previousSibling.previousSibling.value)">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <path d="M25 20 L65 45 L25 70"></path>
          </svg>
        </div>
        <div class="histbtn normCol square" onclick="moveUp(this)">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <path d="M45 20 L65 50 L50 50 L50 70 L40 70 L40 50 L25 50"></path>
          </svg>
        </div>
        <div class="togglegroup" onclick="toggleGT()">
          <div class="toggleitem grid normCol">
            <svg width="90" height="90" viewBox="0 0 90 90">
              <rect x="15" y="15" width="25" height="25"></rect>
              <rect x="50" y="15" width="25" height="25"></rect>
              <rect x="15" y="50" width="25" height="25"></rect>
              <rect x="50" y="50" width="25" height="25"></rect>
            </svg>
          </div>
          <div class="toggleitem table normCol">
            <svg width="90" height="90" viewBox="0 0 90 90">
              <rect x="15" y="25" width="60" height="5"></rect>
              <rect x="15" y="42" width="60" height="5"></rect>
              <rect x="15" y="60" width="60" height="5"></rect>
            </svg>
          </div>
        </div>
      </div>
      <div class="innercontent">
        <div class="sidebar">
          <div class="sidelinkwrapper"></div>
        </div>
        <div class="filecontent"></div>
      </div>
    </div>
    <div id="svgbuffer" style="display:none">
      <svg class="err_icon" width="90" height="90" viewBox="0 0 90 90">
        <path d="M5 80 L45 10 L85 80 Z" fill="#fe0" stroke="#d00" stroke-width="6"></path>
        <path d="M40 35 L50 35 L48 60 L42 60" fill="#a00"></path>
        <path d="M42 64 L48 64 L48 72 L42 72" fill="#a00"></path>
      </svg>
      <svg class="info_icon" width="90" height="90" viewBox="0 0 90 90">
        <circle cx="45" cy="45" r="40" fill="#4af" stroke="#46f" stroke-width="5"></circle>
        <path d="M37 20 L53 20 L50 55 L40 55" fill="white"></path>
        <path d="M40 62 L50 62 L50 72 L40 72" fill="white"></path>
      </svg>
      <svg class="cog_icon" width="90" height="90" viewBox="0 0 90 90">
        <path fill="none" stroke-width="5"></path>
        <circle cx="45" cy="45" r="10" fill="none" stroke-width="5"></circle>
      </svg>
    </div>
    <div id="consolebuffer" style="display:none">
      <div class="console">
        <div class="inputbox">
          <div class="dir">P:\picturelements.github.io>&nbsp;</div>
          <div>
            <input class="input" spellcheck="false" autocomplete="off"></input>
            <pre class="input_output"></pre>
            <span class="caret">
              <div class="backcaret"></div>
              <div class="frontcaret"></div>
            </span>
          </div>
        </div>
      </div>
    </div>
    <div id="loadscreenbuffer" style="display:none">
      <div id="loadercontainer">
        <div class="loader"></div>
        <div class="loader2"></div>
        <div class="loader3"></div>
        <p class="loadmsg">Starting PeOS...</p>
      </div>
    </div>
  </body>
</html>


      <!--<div class="desktoplink">
        <div class="dimg"></div>
        <p class="ddesc">Home</p>
      </div>
      </div>
      <div class="window">
        <div class="infobar">
          <div class="close" title="Close">X</div>
          <div class="max" title="Maximize">◳</div>
          <div class="min" title="Minimize">_</div>
          <div class="wintitle">Test Window</div>
        </div>
        <iframe class="content" src="https://picturelements.github.io/sudokuSolver"></iframe>
        <div class="resize"></div>
      </div>-->


<!--
<div class="result">
          <div class="resultimg"></div>
          <div class="resultname">title here</div>
          <div class="keywords">insert keywords here</div>
        </div>
-->


      <!--<div class="taskbaricon" onclick=selectIcon(event,1,true) id="null" type="1" activelevel="0" title="Home">
        <div class="smallicon" style="background-image:url(https://picturelements.github.io/images/win_icons/home.png);"></div>
      </div>
      <div class="taskbaricon" onclick=selectIcon(event,2,true) id="null" type="2" activelevel="0" title="Sudoku Solver">
        <div class="smallicon" style="background-image:url(https://picturelements.github.io/images/win_icons/sudokusolver.png);"></div>
      </div>
      <div class="taskbaricon" onclick=selectIcon(event,3,true) id="null" type="3" activelevel="0" title="Mandelbrot Generator">
        <div class="smallicon" style="background-image:url(https://picturelements.github.io/images/win_icons/mandelbrot.png);"></div>
      </div>-->
