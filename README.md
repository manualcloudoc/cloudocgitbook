---
description: 문서 반출 기능을 소개합니다.
---

# 문서반출 기능 사용하기

### <mark style="color:$primary;">문서반출 절차</mark>

로컬저장금지 정책 등 관리자가 설정한 DiskLock정책에 따라, 고정 디스크로의 파일 복사/이동과 웹 브라우저, 이메일, 메신저 등에서의 파일 첨부가 금지될 수 있습니다.  이 경우 문서를 메일 또는 메신저에 첨부하여 전달하거나 이동식 디스크 등에 저장하여 외부에서 사용하기 위해서는 승인권자의 결재 단계를 포함한 문서반출 절차를 거쳐야 합니다.

문서반출의 기본적인 절차는 다음과 같습니다.

<table><thead><tr><th width="189">단계</th><th>내용</th></tr></thead><tbody><tr><td><strong>1. 문서반출 신청</strong></td><td>사용자가 반출하고자 하는 파일/폴더를 선택하여 반출을 신청합니다. 이때 문서의 보안 수준에 따라 <strong>반출 종류(공개반출/보안반출)</strong> 을 지정해야 하며, 관리자의 설정에 따라 <strong>승인권자</strong>와 <strong>결재 방식(선결재/후결재)</strong>을 선택할 수 있습니다.</td></tr><tr><td><strong>2. 승인권자의 반출 승인</strong></td><td>승인권자는 문서반출 신청 내역을 확인하고 해당 요청을 승인 또는 반려할 수 있습니다. <strong>선결재</strong>의 경우 반출 승인이 완료된 후 다음 단계가 진행되며, <strong>후결재</strong>인 경우에는 승인 여부와 상관없이 곧바로 다음 단계가 진행됩니다.</td></tr><tr><td><strong>3. 반출 폴더/파일 생성</strong></td><td>해당 문서함의 <strong>DOC_EXPORT</strong> 폴더 내에 폴더명이 ‘해당 폴더의 생성 일시’인 폴더가 생성되고, 생성된 폴더 내에 반출이 승인된 파일/폴더가 복사됩니다.</td></tr><tr><td><strong>4. 문서의 반출</strong></td><td><strong>DOC_EXPORT</strong> 폴더 내 반출용 파일/폴더를 메일이나 메신저 등에 첨부하거나 반출 가능한 디스크로 다운로드/복사할 수 있습니다. 이때 반출 종류와 관리자의 설정에 따라 반출 가능 범위가 달라집니다.지정된 반출 기한 만료 시 반출용 파일/폴더의 사용이 제한됩니다.</td></tr></tbody></table>

<figure><img src=".gitbook/assets/문서반출 기능 소개_claude.png" alt=""><figcaption></figcaption></figure>

### <mark style="color:$primary;">문서반출 설정</mark>

문서반출의 절차 및 반출 범위는 문서반출 신청 시 지정되는 결**재 방식, 반출 종류, 반출 기간, 반출 가능한 디스크**에 따라 달라집니다. 이때 사용자가 선택할 수 있는 결재 방식, 반출 기간, 반출 가능한 디스크의 범위는 관리자가 사용자/부서별로 설정한 **문서반출 정책**에 따라 제한됩니다.

{% hint style="warning" icon="square-poll-horizontal" %}
결재 방식에 대한 설명은 [**승인권자 및 결재 방식 소개**](/broken/pages/bwMwfk8hYg39AgtuAA4c)를 참고합니다.
{% endhint %}

#### 반출 종류

문서반출 시 반출 가능한 디스크의 선택 및 파일 첨부가 가능한 **공개반출**과 반출 범위가 반출 보안디스크(이하 반출디스크)로만 제한되는 **보안반출**이 있습니다. 반출 종류는 사용자가 문서반출 신청 시 선택하게 되며, 보안성이 중요한 기밀 문서의 경우 **보안반출**을 권장합니다.

<table><thead><tr><th width="126">반출 종류</th><th width="300">반출 범위</th><th>반출 가능한 디스크 목록</th></tr></thead><tbody><tr><td><strong>공개반출</strong></td><td><ul><li> 반출 신청 시 반출 가능한 디스크 선택 가능</li></ul></td><td><ul><li>반출디스크</li><li>고정디스크 </li><li>CD-ROM </li><li>이동식 디스크 </li><li>네트워크 디스크</li></ul></td></tr><tr><td><strong>보안반출</strong></td><td><ul><li>반출디스크로만 반출 가능</li><li>반출용 파일의 메일/메신저 첨부 불가</li></ul></td><td><ul><li>반출디스크</li></ul></td></tr></tbody></table>

{% hint style="warning" icon="square-poll-horizontal" %}
공개반출 시에도 관리자의 정책 설정에 따라 부서/사용자 별로 반출 가능한 디스크 종류가 제한될 수 있습니다.
{% endhint %}

{% hint style="warning" icon="square-poll-horizontal" %}
반출디스크(반출 보안디스크)는 고정디스크(또는 설정에 따라 이동식 디스크) 내에 생성되는 보안이 강화된 가상 드라이브입니다. 반출디스크에 대한 설명은 [**보안디스크 소개**](/broken/pages/1gutlB8mHNPCmkU41TvT)를 참고하세요
{% endhint %}

#### 반출 기간

문서반출 신청 시 반출할 폴더/파일을 사용할 수 있는 기간을 지정할 수 있습니다. 이때 반출 기간의 범위는 관리자의 정책 설정에 따라 제한됩니다. 지정된 반출 기간이 경과하면, DOC\_EXPORT 폴더 내 생성된 반출 폴더/파일은 자동 삭제되어 사용할 수 없습니다.

