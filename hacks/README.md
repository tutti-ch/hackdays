<section class="nes-container t-grey with-title">
    <h2 class="title tred">List of Planned Hacks</h2>
    <table class="nes-table is-bordered is-centered">
        <thead>
            <th>Name</th>
            <th>Summary</th>
        </thead>
        <tbody>
    {% for page in site.pages %}
        {% if page.resource == true and page.archived == false %}
        {% for pc in page.categories %}
            {% if pc == "hack" %}
                <tr>
                    <td><a href="/hackdays{{ page.url }}">{{ page.hackname }}</a></td>
                    <td>{{ page.quicksummary }}</td>
                </tr>
            {% endif %}   <!-- cat-match-p -->
        {% endfor %}  <!-- page-category -->
        {% endif %}   <!-- resource-p -->
    {% endfor %}  <!-- page -->
        </tbody>
    </table>
</section>

<i class="nes-squirtle"></i>

<section class="nes-container t-grey with-title">
    <h2 class="title tred">List of past Hacks</h2>
    <table class="nes-table is-bordered is-centered">
        <thead>
            <th>Name</th>
            <th>Award</th>
            <th>Summary</th>
        </thead>
        <tbody>
    {% for page in site.pages %}
        {% if page.resource == true and page.archived == true %}
        {% for pc in page.categories %}
            {% if pc == "hack" %}
                <tr>
                    <td><a href="/hackdays{{ page.url }}">{{ page.hackname }}</a></td>
                    <td>
                    {% if page.award == "top" %}
                        <i class="nes-icon is-medium star" />
                    {% else %}
                        <i class="nes-icon is-medium star is-transparent" />
                    {% endif %}
                    </td>
                    <td>{{ page.quicksummary }}</td>
                </tr>
            {% endif %}   <!-- cat-match-p -->
        {% endfor %}  <!-- page-category -->
        {% endif %}   <!-- resource-p -->
    {% endfor %}  <!-- page -->
        </tbody>
    </table>

</section>

<i class="nes-bulbasaur"></i>

<section class="nes-container t-grey with-title">
    <h2 class="title tred">Hints for Adding Your Hack</h2>

    <ul class="nes-list is-disc">
        <li>Put your hack description in the /hackdays/hacks/ directory of this git repository</li>
        <li>You can use <a href="/hackdays/hacks/dashboard">this page</a> as a template. Make sure to use the meta tags at the top of the file (see the template for clues)</li>
    </ul>

</section>
