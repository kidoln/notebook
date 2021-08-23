#+TITLE: Contents

** 医学技术新趋势
:PROPERTIES:
:heading: true
:END:
*** [[麦肯锡医学]]
** 其他内容
:PROPERTIES:
:heading: true
:END:
*** [[微软同学聚会]]
*** [[测试页面]]
**
#+BEGIN_QUERY
{:title "📅 Next 7 days' deadline or schedule"
    :query [:find (pull ?block [*])
            :in $ ?start ?next
            :where
            (or
              [?block :block/scheduled ?d]
              [?block :block/deadline ?d])
            [(> ?d ?start)]
            [(< ?d ?next)]]
:inputs [:today :7d-after]
:collapsed? false}
#+END_QUERY
**
**