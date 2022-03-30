
<style>
 summary {
  padding: 4px;
  border: none;
  font-size: initial;
}
 td {
  padding: 4px;
  border: none;
  font-size: initial;
}
 details  {
  padding: 4px;
  font-size: 80%;
}
</style>
<table style="table-layout: fixed; width:100%; margin:auto; text-align:center">
<thead>
<tr>
<td style="text-align:center">Date</td>
<td style="text-align:center">Speaker</td>
<td style="text-align:center">Title</td>
</tr>
</thead>
<tbody>
<style>
      tr:nth-of-type(even) {
      background-color:#ebf5f8;
    }

</style>
{% assign sorted = {{datafile}}  %}
{% for X in sorted %}
 <tr future-date="{{ X.date | date: '%Y-%m-%d' }}">

<td> {% if X.cancelled %} <s>{{ X.date | date: "%-d %b %Y" }}</s> {% else %} {{ X.date | date: "%-d %b %Y" }} {% endif %}</td>
  <td>
  {% if X.url %} <a href="{{X.url}}">{{X.speaker}} </a> {% else %} {{X.speaker | markdownify }}   {% endif %}</td>

  <td style="text-align:left"> {% if X.teams %}<a href="{{X.teams}}"><font color="red">Teams</font></a>
   {% endif %}  

  {% if X.abstract %}
  <details>  
  <summary>
  {% if X.inred %} <font color="red"> {{X.inred }} </font>  {% endif %}
   {{X.title}}
  
   </summary>
    <p>
    {{X.abstract | markdownify}}
   </p>
    </details>
 {% else %}
  {% if X.inred %} <font color="red"> {{ X.inred }} </font>   {% endif %}

    {% if X.title %} <br /> {{X.title}} {% endif %}
  {% endif %}
  </td>

  </tr>
  
{% endfor %}
</tbody>
</table>
