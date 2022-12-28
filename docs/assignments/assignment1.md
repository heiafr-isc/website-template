---
title: Travail Pratique 1
tpno: 1
---

{% set exno = namespace(no=0) %}
{% set subno = namespace(no=0) %}
{% macro ex() -%}
{% set exno.no = exno.no + 1 %}**Exercice #{{ exno.no }}**{% set subno.no = 0 %}
{%- endmacro %}
{% macro exx() -%}
**{% set subno.no = subno.no + 1 %}Exercice #{{ exno.no }}.{{ subno.no }}**
{%- endmacro %}

Lorem ipsum dolor sit amet ...

``` go
{! include "assignment1/hello.go" !}
```

!!! note "Note"
    ``` go
    {! include "assignment1/hello.go" !}
    ```

{{ ex() }}: Bla
{% if assignment_show_solution >= page.meta.tpno %}
??? success "Solution"
    Solution ...
{% endif %}

{{ exx() }} : Bla Bla

{% if assignment_show_solution >= page.meta.tpno + 0.5 %}
??? success "Solution"
    Solution ...
{% endif %}

{{ ex() }}: Bla
{% if assignment_show_solution >= page.meta.tpno %}
??? success "Solution"
    Solution ...
{% endif %}

{{ exx() }} : Bla Bla

{% if assignment_show_solution >= page.meta.tpno + 0.5 %}
??? success "Solution"
    Solution ...
{% endif %}

{{ exx() }} : Bla Bla

{% if assignment_show_solution >= page.meta.tpno + 0.5 %}
??? success "Solution"
    Solution ...
{% endif %}
