---
course_id: 16-90-computational-methods-in-aerospace-engineering-spring-2014
layout: course_section
parent_title: 1.8 Multi-Step Methods
title: 1.8 Multi-Step Methods
type: course
uid: 75e73977a306f5532134b4e0a24fdb81

---

*   [<Multi-Step Methods]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods)
*   [1.8.1Adams-Bashforth Methods]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods)
*   [1.8.2Adams-Moulton Methods]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods/1690r-adams-moulton-methods)
*   [1.8.3Backwards Differentiation Methods]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods/1690r-backwards-differentiation-methods)
*   [1.8.4Backwards Differentiation Excercise]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods/1690r-backwards-differentiation-excercise)
*   [\>Backwards Differentiation Methods]({{< baseurl >}}/sections/numerical-integration-of-ordinary-differential-equations/multi-step-methods/1690r-backwards-differentiation-methods)

1.8.2 Adams-Moulton Methods
---------------------------

[Measurable Outcome 1.12]({{< baseurl >}}/sections/measurable-outcome-index/#anchorMO112), [Measurable Outcome 1.15]({{< baseurl >}}/sections/measurable-outcome-index/#anchorMO115), [Measurable Outcome 1.17]({{< baseurl >}}/sections/measurable-outcome-index/#anchorMO117), [Measurable Outcome 1.18]({{< baseurl >}}/sections/measurable-outcome-index/#anchorMO118), [Measurable Outcome 1.19]({{< baseurl >}}/sections/measurable-outcome-index/#anchorMO119)

Adams-Moulton methods are implicit methods of the form,

| \\\[v^{n+1} - v^{n} = {\\Delta t}\\sum \_{i=0}^ s \\beta \_ i f^{n+1-i}.\\\] | (1.137) 

These methods use the same time derivative approximation as the Adams-Bashforth methods, however they include the \\(n+1\\) value of \\(f\\).

|  {{< br >}}{{< br >}} \\(p\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\beta \_0\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\beta \_1\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\beta \_2\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\beta \_3\\) {{< br >}}{{< br >}}  |
|  {{< br >}}{{< br >}} 1 {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} 1 {{< br >}}{{< br >}}  | &nbsp; |
|  {{< br >}}{{< br >}} 2 {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{1}{2}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{1}{2}\\) {{< br >}}{{< br >}}  | &nbsp; |
|  {{< br >}}{{< br >}} 3 {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{5}{12}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{8}{12}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(-\\frac{1}{12}\\) {{< br >}}{{< br >}}  | &nbsp; |
|  {{< br >}}{{< br >}} 4 {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{9}{24}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{19}{24}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(-\\frac{5}{24}\\) {{< br >}}{{< br >}}  |  {{< br >}}{{< br >}} \\(\\frac{1}{24}\\) {{< br >}}{{< br >}}  

**Table 3**: Coefficients for Adams-Moulton methods. Note: the \\(p=1\\) method is the backward Euler method, and the \\(p=2\\) method is the Trapezoidal method.

The coefficients for the first through fourth order methods are given in the table above.

![The graph shows the shrinking, mostly non-overlapping, Adams-Moulton stability regions for p=1 through p=4 methods.](/coursemedia/16-90-computational-methods-in-aerospace-engineering-spring-2014/c5b34db6e9059a956bed1aab4aa2492b_am_stab.png)

**Figure 1.20**: Adams-Moulton stability regions for \\(p=1\\) through \\(p=4\\) methods. Note: \\(p=1\\) is stable outside of contour, the \\(p=2\\) integrator is stable in the left-half plane, and \\(p\\geq 3\\) are stable inside their respective contours.

The stability boundary for these methods are shown in Figure [1.20](/coursemedia/16-90-computational-methods-in-aerospace-engineering-spring-2014/c5b34db6e9059a956bed1aab4aa2492b_am_stab.png). While the stability regions are larger than the Adams-Bashforth methods, for \\(p>2\\) the methods have bounded stability regions. Thus, they will not be appropriate for stiff problems.

BackMulti-Step Methods ContinueBackwards Differentiation Methods