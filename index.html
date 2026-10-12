//global vars
var categories = [];
var install_button;
var uninstall_button;
var devstring;
var pkg_links = [];
var download_button;
var control_button;
var pbc;
var pb;
var pbt;
var reopen_game_url;
var reopen_game_id;
var games_json;
var pkglink;
var progress_update_interval;

function set_category() {
    for (i = 0; i < categories.length; i++) {
        document.getElementById("filter_" + i).checked = false;
    }
    document.getElementById("filter").hidden = true;
    document.getElementById("filter_" + categories.indexOf(category)).checked = true;
    search("pkgs.json");
}

function search(url) {
    var filters = [];
    for (i = 0; i < categories.length; i++) {
        if (document.getElementById("filter_" + i).checked == true) {
            filters.push(categories[i]);
        }
    }
    for (i = 0; i < games_json.length; i++) {
        var element = document.getElementById("game_" + i);
        if (element != null) {
            element.parentNode.removeChild(element);
        }
    }

    for (i = 0; i < games_json.length; i++) {
        if (games_json[i].categories.some(r => filters.includes(r)) && (games_json[i].name.toUpperCase().includes(document.getElementById("searchbar").value.toUpperCase()) || games_json[i].titleid.toUpperCase().includes(document.getElementById("searchbar").value))) {
            var x = document.createElement("DIV");
            x.setAttribute("id", "game_" + i);
            x.setAttribute("class", "game");
            x.setAttribute("onclick", "opengame(\"pkgs.json\", " + i + ")");
            var y = document.createElement("IMG");
            y.setAttribute("class", "icon");
            y.setAttribute("src", games_json[i].icon);
            var z = document.createTextNode(games_json[i].name);
            x.appendChild(y);
            x.appendChild(document.createElement("br"));
            x.appendChild(z);
            document.getElementById("center").appendChild(x);
        }
    }
}

function interval(func, wait, times) {
    var interv = function(w, t) {
        return function() {
            if (typeof t === "undefined" || t-- > 0) {
                setTimeout(interv, w);
                try {
                    func.call(null);
                } catch (e) {
                    t = 0;
                    throw e.toString();
                }
            }
        };
    }(wait, times);
    setTimeout(interv, wait);
}

function setCookie(cname, cvalue, exdays) {
    var d = new Date();
    d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
    var expires = "expires=" + d.toGMTString();
    document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}

function getCookie(cname) {
    var name = cname + "=";
    var decodedCookie = decodeURIComponent(document.cookie);
    var ca = decodedCookie.split(';');
    for (var i = 0; i < ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0) == ' ') {
            c = c.substring(1);
        }
        if (c.indexOf(name) == 0) {
            return c.substring(name.length, c.length);
        }
    }
    return "";
}

function compare(a, b) {
    if (a.name.toUpperCase() < b.name.toUpperCase()) return -1;
    if (a.name.toUpperCase() > b.name.toUpperCase()) return 1;
    return 0;
}

function request(url) {
    reopen_game_url = "pkgs.json";
    var xhttp = new XMLHttpRequest();
    xhttp.onreadystatechange = function() {
        if (this.readyState == 4 && this.status == 200) {
            games_json = JSON.parse(xhttp.responseText);
            games_json.sort(compare);
            for (i = 0; i < games_json.length; i++) {
                for (j = 0; j < games_json[i].categories.length; j++) {
                    if (!categories.includes(games_json[i].categories[j])) {
                        categories.push(games_json[i].categories[j])
                    }
                }

                var x = document.createElement("DIV");
                x.setAttribute("id", "game_" + i);
                x.setAttribute("class", "game");
                x.setAttribute("onclick", "opengame(\"pkgs.json\", " + i + ")");
                var y = document.createElement("IMG");
                y.setAttribute("class", "icon");
                y.setAttribute("src", games_json[i].icon);
                var z = document.createTextNode(games_json[i].name);
                x.appendChild(y);
                x.appendChild(document.createElement("br"));
                x.appendChild(z);
                document.getElementById("center").appendChild(x);
            }

            for (i = 0; i < categories.length; i++) {
                var x = document.createElement("DIV");
                x.setAttribute("class", "filter")
                var y = document.createElement("INPUT");
                y.setAttribute("checked", "true");
                y.setAttribute("class", "setcursor");
                y.setAttribute("onclick", "search(\"pkgs.json\")");
                y.setAttribute("id", "filter_" + i);
                y.setAttribute("type", "checkbox");
                var z = document.createElement("LABEL");
                z.setAttribute("class", "setcursor");
                z.innerText = categories[i] + ": ";
                z.setAttribute("for", y.id)
                x.appendChild(z);
                x.appendChild(y);
                document.getElementById("filter").appendChild(x);
            }

            if (typeof category !== 'undefined') {
                set_category();
            }
        }
    };
    xhttp.open("GET", "pkgs.json", true);
    xhttp.send();
}

function opengame(url, gameid) {
    reopen_game_id = gameid;
    window.location.href = "game.html?id=" + gameid + "&url=pkgs.json";
}
