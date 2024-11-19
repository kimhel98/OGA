# Query the Corpus

The corpus can be queried through the original XML files or Annis. 
In either case, one must know the labels used to encode annotations
(for example, "v" stands for verbs and "n" for nouns). The files in this
folder document all of them.

# Annis Query Examples

Annis query language is documentated on https://korpling.github.io/ANNIS/4/user-guide/aql/index.html. The following are query examples that can be used as templates:

[tok="Ἀχαιοὶ" @* work_date=/(p1_1|p1_2)/](https://annis.varro.informatik.uni-leipzig.de/?id=4da2728e-82d7-480b-94d0-c20febd22504#_q=dG9rPSLhvIjPh86xzrnOv-G9tiIgQCogd29ya19kYXRlPS8ocDFfMXxwMV8yKS8K&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[lemma="ἀθηναῖος" @* work_date=/(m5_1|m5_2|m4_1|m4_2)/](https://annis.varro.informatik.uni-leipzig.de/?id=52281da9-9508-4ac2-be14-ce79c5731e2a#_q=bGVtbWE9IuG8gM64zrfOvc6x4b-Wzr_PgiIgQCogd29ya19kYXRlPS8obTVfMXxtNV8yfG00XzF8bTRfMikvCgo&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[lemma="ἀθηναῖος" @* work_date=/(p1_1|p1_2|p2_1|p2_2|p1_1|p1_2)/](https://annis.varro.informatik.uni-leipzig.de/?id=433e2997-85ed-49be-bbe1-858ff27c06d7#_q=bGVtbWE9IuG8gM64zrfOvc6x4b-Wzr_PgiIgQCogd29ya19kYXRlPS8ocDFfMXxwMV8yfHAyXzF8cDJfMnxwMV8xfHAxXzIpLwoK&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[lemma="ἀθηναῖος" @* author="Thucydides"](https://annis.varro.informatik.uni-leipzig.de/?id=79e496e6-79f3-4d6b-bd87-4d8dfc68402f#_q=bGVtbWE9IuG8gM64zrfOvc6x4b-Wzr_PgiIgQCogYXV0aG9yPSJUaHVjeWRpZGVzIgoK&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[pos="v" _ident_ cts=/3_.*/ @* author="Homer" _ident_ title="Iliad"](https://annis.varro.informatik.uni-leipzig.de/?id=d70ea7e5-fcbd-42fc-9c76-6c2eb45c0c40#_q=cG9zPSJ2IiBfaWRlbnRfIGN0cz0vM18uKi8gQCogYXV0aG9yPSJIb21lciIgX2lkZW50XyB0aXRsZT0iSWxpYWQiCg&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[pos="v" _ident_ cts=/3_.*/ @* urn_cts_author="tlg0012" _ident_ urn_cts_work="tlg001"
](https://annis.varro.informatik.uni-leipzig.de/?id=92b6bc7a-2246-4a46-873a-e6fcf21f5d98#_q=cG9zPSJ2IiBfaWRlbnRfIGN0cz0vM18uKi8gQCogdXJuX2N0c19hdXRob3I9InRsZzAwMTIiIF9pZGVudF8gdXJuX2N0c193b3JrPSJ0bGcwMDEiCg&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)

[pos="v" _ident_ mood="i" ->dep[dep_fnc="OBJ"] pos="n" & #3 .1,3 #2 @* work_date=/(p1_1|p1_2)/
](https://annis.varro.informatik.uni-leipzig.de/?id=fe33e671-1738-4ca0-bf84-d69f58c1a9b7#_q=cG9zPSJ2IiBfaWRlbnRfIG1vb2Q9ImkiIC0-ZGVwW2RlcF9mbmM9Ik9CSiJdIHBvcz0ibiIgJiAjMyAuMSwzICMyIEAqIHdvcmtfZGF0ZT0vKHAxXzF8cDFfMikvCg&ql=aql&_c=b2dhX3YwLjIuMF81LG9nYV92MC4yLjBfMyxvZ2FfdjAuMi4wXzQsb2dhX3YwLjIuMF8xLG9nYV92MC4yLjBfMg&cl=5&cr=5&s=0&l=10&)