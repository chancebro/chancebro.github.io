---
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume/
  - /resume.html
---

{% assign cv = site.data.cv %}

# {{ cv.basics.name }}

{% if cv.basics.label and cv.basics.label != "" %}
**{{ cv.basics.label }}**
{% endif %}

{% if cv.basics.summary and cv.basics.summary != "" %}
{{ cv.basics.summary }}
{% endif %}

{% if cv.basics.location.city and cv.basics.location.city != "" %}
**Location:** {{ cv.basics.location.city }}, {{ cv.basics.location.region }}  
{% endif %}

{% if cv.basics.email and cv.basics.email != "" %}
**Email:** [{{ cv.basics.email }}](mailto:{{ cv.basics.email }})  
{% endif %}

{% if cv.basics.website and cv.basics.website != "" %}
**Website:** [{{ cv.basics.website }}]({{ cv.basics.website }})
{% endif %}

{% if cv.basics.profiles.size > 0 %}
<p>
{% for profile in cv.basics.profiles %}
{% if profile.url and profile.url != "" %}
<a href="{{ profile.url }}">{{ profile.network }}</a>{% unless forloop.last %} · {% endunless %}
{% endif %}
{% endfor %}
</p>
{% endif %}

<!--
CV PDF를 files/Chanhyeong_Cho_CV.pdf에 업로드한 다음
아래 줄의 주석을 해제하면 다운로드 버튼이 표시됩니다.

[Download CV as PDF](/files/Chanhyeong_Cho_CV.pdf){: .btn .btn--primary }
-->

---

## Education

{% for edu in cv.education %}

### {{ edu.studyType }}{% if edu.area and edu.area != "" %} in {{ edu.area }}{% endif %}

**{{ edu.institution }}**  
{{ edu.startDate }} –
{% if edu.endDate and edu.endDate != "" %}
{{ edu.endDate }}
{% else %}
Present
{% endif %}

{% if edu.note and edu.note != "" %}
{{ edu.note }}
{% endif %}

{% endfor %}
---

## Research Experience

{% for job in cv.work %}

### {{ job.position }}

**{% if job.url and job.url != "" %}[{{ job.name }}]({{ job.url }}){% else %}{{ job.name }}{% endif %}**  
{{ job.startDate }} –
{% if job.endDate and job.endDate != "" %}
{{ job.endDate }}
{% else %}
Present
{% endif %}

{% if job.summary and job.summary != "" %}
{{ job.summary }}
{% endif %}

{% if job.highlights.size > 0 %}
{% for highlight in job.highlights %}
- {{ highlight }}
{% endfor %}
{% endif %}

{% endfor %}

---

## Research Interests

{% for interest in cv.interests %}

### {{ interest.name }}

{% if interest.keywords.size > 0 %}
{{ interest.keywords | join: " · " }}
{% endif %}

{% endfor %}

---

## Publications

{% for publication in cv.publications %}

### {{ forloop.index }}. {{ publication.name }}

**{{ publication.publisher }}**  
{% if publication.releaseDate and publication.releaseDate != "" %}
{{ publication.releaseDate }}
{% endif %}

{% if publication.summary and publication.summary != "" %}
{{ publication.summary }}
{% endif %}

{% if publication.website and publication.website != "" %}
[Paper / DOI]({{ publication.website }}){: .btn .btn--small }
{% endif %}

{% endfor %}

---

## Conference Presentations

{% for presentation in cv.presentations %}

### {{ presentation.name }}

**{{ presentation.event }}**  
{{ presentation.date }}  
{{ presentation.location }}

{% if presentation.description and presentation.description != "" %}
{{ presentation.description }}
{% endif %}

{% endfor %}

---

## Patents

{% for patent in cv.patents %}

### {{ patent.name }}

**{{ patent.number }}**  
{{ patent.date }}

{% if patent.inventors.size > 0 %}
**Inventors:** {{ patent.inventors | join: ", " }}
{% endif %}

{% if patent.summary and patent.summary != "" %}
{{ patent.summary }}
{% endif %}

{% endfor %}

---

## Awards and Honors

{% for award in cv.awards %}

### {{ award.title }}

**{{ award.awarder }}**  
{{ award.date }}

{% if award.summary and award.summary != "" %}
{{ award.summary }}
{% endif %}

{% endfor %}

---





## Research Vision

My research seeks to reconcile privacy, security, and accountability
across digital financial systems and intelligent autonomous
environments.

In digital payments, I study accountable anonymous offline electronic
cash systems that preserve user anonymity and transaction unlinkability
during normal operation while supporting selective auditing and tracing
when double spending, money laundering, or other illicit financial
activity is confirmed. Through this work, I aim to contribute to
privacy-preserving payment infrastructures for electronic cash, CBDCs,
and stablecoin-based systems.

The same fundamental challenge also appears in IIoT and autonomous
systems. Devices should be able to prove that they are authorized
without repeatedly revealing persistent identifiers, while compromised
or malicious devices must still be efficiently revoked or investigated.
Building on my work in accountable anonymity, I am extending my research
to privacy-preserving authentication, revocation, and selective data
protection for IIoT, robots, and Physical AI systems.

My long-term goal is to develop cryptographic mechanisms that allow
legitimate users and devices to operate without excessive surveillance
while enabling narrowly scoped and technically enforceable
accountability when misuse occurs. Through this research, I seek to
support both safer digital financial systems and trustworthy autonomous
environments.
