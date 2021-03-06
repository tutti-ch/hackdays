<section class="nes-container t-grey with-title">
    <h2 class="title tred">About the next event</h2>
    <ul class="nes-list is-disc">
        <li>Pitch: 21st of June.</li>
        <li>Hacking time: 26th and 27th of June.</li>
        <li>Awards: 28th of June.</li>
    </ul>
</section>

<i class="nes-icon is-large heart"></i>

<section class="nes-container t-grey with-title">
    <h2 class="title tred">Contents</h2>
    <ul class="nes-list is-disc">
        <li><a href="./whoami">Who's Who?</a></li>
        <li><a href="./hacks/">List of Planned Hacks</a></li>
    </ul>
</section>

<i class="nes-ash"></i>

<section class="nes-container t-grey with-title">
    <h2 class="title tred">Step 1: Add Yourself to the Who's Who List</h2>
    <p>Get yourself listed on <a href="/hackdays/whoami">Who am I?</a></p>
    <ol>
        <li><code>$ git clone git@github.com:tutti-ch/hackdays.git</code></li>
        <li><code>$ cd ./hackdays; git checkout -b &lt;your_name&gt;</code></li>
        <li><code>$ cp ./whoami/marcello.md ./whoami/&lt;your_name&gt;.md</code></li>
        <li><code>$ vi ./whoami/&lt;your_name&gt;.md</code></li>
        <li><code>$ open http://yrlab.zatunen.com/webgl/gbpic/gbpic.html # to gameboyify your profile pic</code></li>
        <li>save the picture to <code>./whoami/pics/&lt;yourname&gt;.png</code> then <code>$ vi ./whoami/&lt;your_name&gt;.md</code> again to link to the image</li>
        <li><code>$ git add &lt;filenames&gt; # add the text file and the image</code></li>
        <li><code>$ git commit -am 'Add myself to whoami'</code></li>
        <li><code>$ git push -u origin your_name</code></li>
        <li>Make a pull request to <a href="https://github.com/tutti-ch/hackdays/">https://github.com/tutti-ch/hackdays/</a></li>
    </ol>
</section>

<section class="nes-container t-grey with-title">
    <h2 class="title tred">Further Hints for Using this Wiki</h2>
    <ul class="nes-list is-disc">
        <li>Create a page about yourself - see <a href="/hackdays/whoami/">whoami</a> for details</li>
        <li>Create a page about project - see <a href="/hackdays/hacks/">hacks</a> for details</li>
        <li>Links to other pages in the wiki should start with /hackdays/</li>
        <li>Submit pull requests if you like to play safe and bug <a href="/hackdays/whoami/marcello">Marcello</a> to merge and get the stuff published</li>
        <li>...or just push to Master if you like to live dangerously ;-)</li>
        <li>I takes about 20-30 seconds after a git push for the site to update</li>
        <li>Use <$ bundle exec jekyll serve> to test changes locally</li>
    </ul>
</section>
