# 문제 상황
- 목표 : 의견 조율을 위한 신속한 웹 프로토타입 개발

👤 페르소나: 멀티미디어 콘텐츠 기업 '네오스트림'의 프론트엔드 개발자 (3년 차)

🏙 배경:
귀사의 콘텐츠 운영팀으로부터 "사내 영상 리뷰 및 승인용 웹 대시보드" 제작을 긴급하게 요청받았습니다.
현재 기획서가 완성되지 않은 상태이며, 기획팀은 "직관적인 UI", 디자인팀은 "트렌디한 다크 모드", 운영팀은 "데이터 밀집형 테이블"을 각각 주장하며 의견이 좁혀지지 않고 있습니다.

💥 핵심 문제:
말로만 회의를 진행하다 보니 서로 상상하는 결과물이 달라 의사결정이 지연되고 있습니다.
오늘 오후 4시 회의 전까지, 실제로 작동하는 형태의 결과물이 없으면 프로젝트 착수가 무기한 연기될 위기입니다.
디자인 툴(Figma 등)로 그리기에는 시간이 부족하고, 버튼 클릭 등 인터랙션이 가능한 HTML/CSS 기반의 퍼블리싱 결과물을 보여줘야만 이해관계자들을 설득할 수 있습니다.

🎯 해결 과제:
요구사항(영상 플레이어 영역, 타임스탬프 댓글 기능, 승인/반려 버튼, 다크 모드 스타일)을 포함한 **단일 페이지 웹 프로토타입 코드(HTML, CSS, JS)**를 AI를 통해 즉시 생성하십시오.
이 코드는 회의 시간 내에 즉석에서 수정 요청을 반영할 수 있을 만큼 구조가 명확해야 합니다.

- 훈련 초점 (힌트)
이 문제는 [코딩 및 프로토타입 생성 / 시각화] 능력을 평가
단순한 텍스트 생성이 아니라, 구체적인 UI/UX 요구사항을 구조화된 언어(코드)로 변환하는 프롬프트 엔지니어링 기술이 필요

---
# 프롬프트 유형 및 선택 이유

1️⃣ 역할 부여(Role-Playing) – 프론트엔드 개발자 역할을 부여해 실제 현업 맥락과 기술적 판단을 반영하기 위함.

2️⃣ 제약 조건(Constraint-Based) – 코드 구조, 기술 스택(HTML/CSS/JS), 시간 제한, 다크 모드 등 구체적 조건을 명확히 하여 실무 적용 가능한 결과물을 확보하기 위함.

3️⃣ 체인 오브 스루트(Chain of Thought) – 복잡한 요구사항(디자인+기능+시간 제약)을 단계적으로 구조화해 오류 없이 완성도 높은 프로토타입을 산출하기 위함.

---
# ✅ 문제 해결 프롬프트
```
당신은 **멀티미디어 콘텐츠 기업 ‘네오스트림’의 프론트엔드 개발자(3년 차)**입니다.
현재 기획이 미완성인 상황에서 사내 영상 리뷰 및 승인용 웹 대시보드의 프로토타입을 오늘 오후 4시까지 시연해야 합니다.
회의 전에 각 팀(기획, 디자인, 운영)의 요구를 시각적으로 보여줄 수 있는 단일 페이지 HTML/CSS/JS 코드를 즉시 완성해야 합니다.

요구사항을 충족하기 위해 단계별로(체인 오브 스루트 방식) 다음 절차를 수행하세요:

1️⃣ 핵심 요구 정리 단계

기획팀: 직관적인 UI

디자인팀: 트렌디한 다크 모드

운영팀: 데이터 밀집형 테이블

공통 요구: 영상 플레이어, 타임스탬프 댓글, 승인/반려 버튼

2️⃣ UI 구조 설계 단계

상단: 프로젝트명과 간단한 내비게이션

중앙: 영상 플레이어 및 타임라인 기반 댓글 패널

하단: 승인/반려 버튼, 테이블(승인 내역 or 피드백 로그)

반응형 구성 유지

3️⃣ 코드 생성 단계 (제약 조건 기반)

기술 스택: HTML + CSS + JS (순수 바닐라)

다크 모드 테마 적용 (배경, 폰트 컬러, 버튼 호버 효과 포함)

JS 코드에는 클릭 이벤트(승인/반려 버튼 클릭 시 상태 변경 알림) 및 타임스탬프 댓글 추가 기능 포함

구조가 명확하고 수정이 용이하도록 주석(comment) 추가

4️⃣ 최종 출력

하나의 HTML 문서 안에 CSS, JS 포함

즉시 브라우저 실행 가능한 형태로 제공

코드 블록 안에만 결과 제시 (설명 문장 제외)

💡 추가 필요 요건:

영상은 실제 파일 대신 샘플 플레이어(<video> 태그, 임의의 썸네일 이미지나 URL)로 구현

테이블은 가상의 데이터 3행 이상 표시

전체 UI는 다크 모드 기준으로 설계

위 단계를 따라, 지금 즉시 실행 가능한 단일 페이지 웹 프로토타입 코드를 완성해 주세요.
```
---
# 프롬프트 실행 결과

```
<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>네오스트림 — 영상 리뷰 대시보드 (프로토타입)</title>
  <style>
    /* ---------------------------
       다크 모드 기본 변수
       --------------------------- */
    :root{
      --bg:#0b0f12;
      --panel:#0f1518;
      --muted:#98a0a6;
      --accent:#4fd1c5; /* 트렌디한 민트톤 */
      --accent-2:#7c3aed; /* 보조 포인트 */
      --danger:#ff6b6b;
      --glass: rgba(255,255,255,0.03);
      --glass-2: rgba(255,255,255,0.02);
      --shadow: 0 6px 18px rgba(2,6,8,0.7);
      --radius:12px;
      --mono: "Helvetica Neue", system-ui, -apple-system, "Segoe UI", Roboto, "Noto Sans KR", "Apple SD Gothic Neo", sans-serif;
    }

    /* ---------------------------
       레이아웃 리셋 & 타이포
       --------------------------- */
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      background:linear-gradient(180deg,var(--bg) 0%, #071011 100%);
      color:#e6eef1;
      font-family:var(--mono);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:20px;
      display:flex;
      align-items:flex-start;
      justify-content:center;
      gap:20px;
    }

    /* ---------------------------
       컨테이너
       --------------------------- */
    .container{
      width:1200px;
      max-width:calc(100% - 40px);
      background:linear-gradient(180deg,var(--panel), #071214);
      border-radius:16px;
      box-shadow:var(--shadow);
      padding:18px;
      display:flex;
      flex-direction:column;
      gap:16px;
    }

    /* ---------------------------
       상단 네비게이션
       --------------------------- */
    .topbar{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
    }
    .brand{
      display:flex;
      align-items:center;
      gap:12px;
    }
    .logo{
      width:44px;height:44px;border-radius:10px;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      display:flex;align-items:center;justify-content:center;
      font-weight:700;color:#081014;box-shadow:0 4px 12px rgba(124,58,237,0.18);
    }
    .project-title{
      display:flex;flex-direction:column;
    }
    .project-title .title{font-size:16px;font-weight:700}
    .project-title .sub{font-size:12px;color:var(--muted)}

    .nav{
      display:flex;gap:10px;align-items:center;
    }
    .nav button{
      background:transparent;border:1px solid var(--glass);padding:8px 12px;border-radius:10px;color:var(--muted);
      cursor:pointer;font-size:13px;
    }
    .nav button:hover{border-color:rgba(255,255,255,0.06);color:var(--accent)}

    /* ---------------------------
       메인 레이아웃: 좌(비디오)우(패널)
       --------------------------- */
    .main{
      display:grid;
      grid-template-columns: 1fr 380px;
      gap:16px;
    }

    /* 비디오 카드 */
    .video-card{
      background:linear-gradient(180deg,var(--glass),var(--glass-2));
      padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);
      display:flex;flex-direction:column;gap:12px;
    }
    .video-area{position:relative;border-radius:10px;overflow:hidden}
    video{
      width:100%;height:auto;background:#000;display:block;
      border-radius:8px;border:1px solid rgba(0,0,0,0.5);
    }

    /* 컨트롤 바(간단) */
    .controls{
      display:flex;align-items:center;gap:10px;justify-content:space-between;
    }
    .controls .left{display:flex;align-items:center;gap:8px}
    .controls button{
      background:transparent;border:1px solid rgba(255,255,255,0.04);padding:8px 10px;border-radius:8px;color:var(--muted);
      cursor:pointer;font-size:13px;
    }
    .controls button.primary{
      background:linear-gradient(90deg,var(--accent),var(--accent-2));border:0;color:#041018;font-weight:700;
    }
    .controls button:hover{transform:translateY(-1px);}

    /* 타임라인 댓글 패널 */
    .timeline{
      display:flex;flex-direction:column;gap:8px;
    }
    .comment-input{
      display:flex;gap:8px;align-items:center;
    }
    .timestamp-capture{
      min-width:96px;padding:10px;border-radius:10px;background:#061213;border:1px solid rgba(255,255,255,0.02);
      display:flex;flex-direction:column;align-items:flex-start;font-size:12px;color:var(--muted)
    }
    .comment-input textarea{
      flex:1;min-height:54px;padding:10px;border-radius:10px;background:transparent;border:1px solid rgba(255,255,255,0.04);color:inherit;
      resize:vertical;font-size:13px;
    }
    .comment-input .actions{display:flex;flex-direction:column;gap:6px}
    .btn{padding:8px 12px;border-radius:8px;border:0;background:rgba(255,255,255,0.03);color:var(--muted);cursor:pointer;font-size:13px}
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.03)}
    .btn.add{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:#041018;font-weight:700}

    .comments-list{margin-top:6px;display:flex;flex-direction:column;gap:8px;max-height:340px;overflow:auto;padding-right:6px}
    .comment-item{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.015));
      padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.02);font-size:13px;display:flex;justify-content:space-between;gap:8px;
    }
    .comment-left{display:flex;gap:8px;align-items:flex-start}
    .time-badge{background:rgba(255,255,255,0.03);padding:6px 8px;border-radius:8px;font-weight:700;color:var(--accent);cursor:pointer}
    .comment-text{color:var(--muted);max-width:620px;word-break:break-word}
    .comment-meta{font-size:12px;color:var(--muted);margin-top:6px}

    /* ---------------------------
       우측 패널: 상태 & 로그 (데이터 밀집형 테이블)
       --------------------------- */
    .side{
      display:flex;flex-direction:column;gap:12px;
    }
    .card{background:linear-gradient(180deg,var(--glass),transparent);padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,0.02)}
    .status-row{display:flex;gap:8px;align-items:center;justify-content:space-between}
    .status-pill{padding:8px 10px;border-radius:999px;background:#051014;border:1px solid rgba(255,255,255,0.03);font-weight:700}
    .small{font-size:13px;color:var(--muted)}

    /* Dense table style */
    table{width:100%;border-collapse:collapse;font-size:13px}
    thead th{font-size:12px;text-align:left;color:var(--muted);padding:8px 6px;border-bottom:1px dashed rgba(255,255,255,0.03)}
    tbody td{padding:8px 6px;border-bottom:1px solid rgba(255,255,255,0.02)}
    tbody tr:hover{background:linear-gradient(90deg, rgba(255,255,255,0.01), transparent)}
    .table-actions button{margin-left:6px;padding:6px 8px;border-radius:8px;border:0;background:rgba(255,255,255,0.03);cursor:pointer;font-size:12px}

    /* 승인/반려 바 */
    .action-bar{display:flex;gap:10px;align-items:center;justify-content:flex-end}
    .action-bar .danger{background:linear-gradient(90deg,var(--danger),#ff8a8a);color:#081014;font-weight:700;border:0}

    /* 토스트 */
    .toast{
      position:fixed;right:24px;bottom:24px;background:#061213;padding:12px 16px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);box-shadow:0 6px 30px rgba(0,0,0,0.6);
      color:var(--muted);font-size:13px;display:none;z-index:1000;
    }

    /* 반응형(간단) */
    @media (max-width:1000px){
      .main{grid-template-columns:1fr}
      .side{order:2}
    }
  </style>
</head>
<body>
  <div class="container" role="application" aria-label="네오스트림 영상 리뷰 대시보드 - 프로토타입">
    <!-- 상단 -->
    <div class="topbar">
      <div class="brand">
        <div class="logo">NS</div>
        <div class="project-title">
          <div class="title">네오스트림 — 영상 리뷰 대시보드</div>
          <div class="sub">프로토타입 • 다크 모드 • 데이터 밀집형 테이블</div>
        </div>
      </div>

      <div class="nav" role="navigation" aria-label="페이지 내비게이션">
        <button>대시보드</button>
        <button>프로젝트 설정</button>
        <button>도움말</button>
      </div>
    </div>

    <!-- 메인 영역 -->
    <div class="main">
      <!-- 좌: 비디오 + 타임라인 댓글 -->
      <div class="video-card">
        <!-- 비디오 플레이어 영역 -->
        <div class="video-area" aria-label="비디오 플레이어">
          <!-- 샘플 비디오: public demo. poster 속성으로 썸네일처럼 보임 -->
          <video id="reviewVideo" controls preload="metadata" poster="https://picsum.photos/seed/neostream/1200/600">
            <source src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4" type="video/mp4" />
            브라우저가 비디오 태그를 지원하지 않습니다.
          </video>
        </div>

        <!-- 간단 컨트롤 -->
        <div class="controls" aria-hidden="false">
          <div class="left">
            <button id="playPause">▶ 재생/일시정지</button>
            <button id="jumpBack">⟲ -10초</button>
            <button id="jumpForward">⟳ +10초</button>
            <div class="small" style="margin-left:8px" id="currentTimeDisplay">00:00 / 00:00</div>
          </div>

          <div style="display:flex;gap:8px;align-items:center">
            <div class="small">테마: 다크 모드</div>
            <button id="toggleCompact" class="btn ghost">테이블 압축 토글</button>
          </div>
        </div>

        <!-- 타임라인 기반 댓글 입력 -->
        <div class="timeline" aria-label="타임스탬프 댓글">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <div style="font-weight:700">타임스탬프 댓글</div>
            <div class="small">현재 재생시간을 캡처하여 댓글과 연결할 수 있습니다.</div>
          </div>

          <div class="comment-input" role="group" aria-label="댓글 입력">
            <div class="timestamp-capture" id="timestampBox">
              <div style="font-size:12px;color:var(--muted)">캡처 시간</div>
              <div id="timestampLabel" style="font-size:16px;font-weight:800;margin-top:6px;color:var(--accent)">00:00</div>
              <div class="comment-meta" style="margin-top:6px">클릭하면 재생 위치로 이동</div>
            </div>

            <textarea id="commentText" placeholder="해당 타임스탬프에 대한 피드백을 입력하세요. (예: 컷 전환이 부드럽지 않습니다)"></textarea>

            <div class="actions" style="min-width:120px">
              <button id="captureTime" class="btn">현재 시간 캡처</button>
              <button id="addComment" class="btn add">댓글 추가</button>
            </div>
          </div>

          <div class="comments-list" id="commentsList" aria-live="polite">
            <!-- 댓글 항목이 동적으로 추가됩니다 -->
          </div>
        </div>
      </div>

      <!-- 우: 사이드 패널 (상태 + 데이터 밀집형 테이블) -->
      <div class="side">
        <!-- 상태 카드 -->
        <div class="card">
          <div class="status-row">
            <div>
              <div style="font-weight:700">상태</div>
              <div class="small">프로젝트: 캠페인 A • 자막 포함</div>
            </div>
            <div style="text-align:right">
              <div class="status-pill" id="approvalStatus">대기중</div>
              <div class="small" style="margin-top:6px">작성자: 운영팀 • 요청일: 2025-11-13</div>
            </div>
          </div>

          <div style="height:12px"></div>

          <!-- 승인/반려 버튼 -->
          <div class="action-bar">
            <button id="rejectBtn" class="btn danger">반려</button>
            <button id="approveBtn" class="btn primary">승인</button>
          </div>
        </div>

        <!-- 피드백 로그 (데이터 밀집형 테이블) -->
        <div class="card" style="flex:1;display:flex;flex-direction:column;gap:10px;min-height:300px">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <div style="font-weight:700">피드백 로그</div>
            <div class="small">최근 활동</div>
          </div>

          <div style="overflow:auto">
            <table id="feedbackTable" aria-label="피드백 로그 테이블">
              <thead>
                <tr>
                  <th style="width:12%">타임스탬프</th>
                  <th style="width:36%">댓글</th>
                  <th style="width:18%">상태</th>
                  <th style="width:18%">작성자</th>
                  <th style="width:16%">행동</th>
                </tr>
              </thead>
              <tbody>
                <!-- 예시 데이터 3행 이상 (가상 데이터) -->
                <tr data-time="00:05">
                  <td><button class="timeLink time-badge">00:05</button></td>
                  <td>인트로 컷에서 색 보정이 어둡습니다. 밝기 +5 필요.</td>
                  <td>대기중</td>
                  <td>민수</td>
                  <td class="table-actions">
                    <button class="btn" onclick="locateTime('00:05')">이동</button>
                    <button class="btn" onclick="markResolved(this)">완료</button>
                  </td>
                </tr>
                <tr data-time="00:21">
                  <td><button class="timeLink time-badge">00:21</button></td>
                  <td>자막 폰트가 너무 작습니다. 16px 권장.</td>
                  <td>대기중</td>
                  <td>지혜</td>
                  <td class="table-actions">
                    <button class="btn" onclick="locateTime('00:21')">이동</button>
                    <button class="btn" onclick="markResolved(this)">완료</button>
                  </td>
                </tr>
                <tr data-time="01:02">
                  <td><button class="timeLink time-badge">01:02</button></td>
                  <td>오디오 레벨 불균형 감지 — BGM 낮춤.</td>
                  <td>대기중</td>
                  <td>운영팀</td>
                  <td class="table-actions">
                    <button class="btn" onclick="locateTime('01:02')">이동</button>
                    <button class="btn" onclick="markResolved(this)">완료</button>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>

          <div style="display:flex;justify-content:space-between;align-items:center">
            <div class="small">총 항목: <span id="tableCount">3</span></div>
            <div class="small">필터: <select id="filterSelect">
              <option value="all">전체</option>
              <option value="pending">대기중</option>
              <option value="done">완료</option>
            </select></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- 토스트 알림 -->
  <div id="toast" class="toast" role="status" aria-live="polite"></div>

  <script>
    /* 
      네오스트림 프로토타입 - 순수 바닐라 JS
      - 기능:
        1) 재생/일시정지 및 -/+10초 점프
        2) 현재시간 표시 및 캡처(타임스탬프)
        3) 타임스탬프 댓글 추가 -> 리스트 + 테이블 동시 반영
        4) 댓글 클릭 시 해당 시간으로 이동
        5) 승인/반려 버튼 : 상태 변경 및 토스트 알림
        6) 테이블 항목 '완료' 처리 및 필터링
      - 구조가 명확하도록 주석을 충분히 표기했습니다.
    */

    // DOM elements
    const video = document.getElementById('reviewVideo');
    const playPauseBtn = document.getElementById('playPause');
    const jumpBackBtn = document.getElementById('jumpBack');
    const jumpForwardBtn = document.getElementById('jumpForward');
    const currentTimeDisplay = document.getElementById('currentTimeDisplay');
    const captureTimeBtn = document.getElementById('captureTime');
    const timestampLabel = document.getElementById('timestampLabel');
    const addCommentBtn = document.getElementById('addComment');
    const commentText = document.getElementById('commentText');
    const commentsList = document.getElementById('commentsList');
    const approvalStatus = document.getElementById('approvalStatus');
    const approveBtn = document.getElementById('approveBtn');
    const rejectBtn = document.getElementById('rejectBtn');
    const toast = document.getElementById('toast');
    const feedbackTable = document.getElementById('feedbackTable').querySelector('tbody');
    const tableCount = document.getElementById('tableCount');
    const filterSelect = document.getElementById('filterSelect');
    const toggleCompact = document.getElementById('toggleCompact');

    // 상태 변수
    let capturedTime = 0; // 초 단위
    let comments = []; // {time:seconds, text, author, id}
    let nextId = 1;
    let compactMode = false;

    // 유틸: 초 -> mm:ss 포맷
    function fmtTime(sec){
      if(isNaN(sec)) sec = 0;
      sec = Math.max(0, Math.floor(sec));
      const m = Math.floor(sec/60).toString().padStart(2,'0');
      const s = (sec%60).toString().padStart(2,'0');
      return `${m}:${s}`;
    }

    // 비디오 메타데이터 로드 이후 전체 길이 표시
    video.addEventListener('loadedmetadata', () => {
      currentTimeDisplay.textContent = `00:00 / ${fmtTime(video.duration)}`;
      // 초기 캡처값은 0
      timestampLabel.textContent = fmtTime(0);
    });

    // 재생 중 시간 갱신
    video.addEventListener('timeupdate', () => {
      currentTimeDisplay.textContent = `${fmtTime(video.currentTime)} / ${fmtTime(video.duration)}`;
    });

    // 재생/일시정지 토글
    playPauseBtn.addEventListener('click', () => {
      if(video.paused) { video.play(); playPauseBtn.textContent = '⏸ 일시정지'; }
      else { video.pause(); playPauseBtn.textContent = '▶ 재생'; }
    });

    // -10초, +10초 버튼
    jumpBackBtn.addEventListener('click', () => { video.currentTime = Math.max(0, video.currentTime - 10); });
    jumpForwardBtn.addEventListener('click', () => { video.currentTime = Math.min(video.duration || 0, video.currentTime + 10); });

    // 현재 시간 캡처 (타임스탬프)
    captureTimeBtn.addEventListener('click', () => {
      capturedTime = Math.floor(video.currentTime || 0);
      timestampLabel.textContent = fmtTime(capturedTime);
      showToast(`현재 시간 ${fmtTime(capturedTime)}이(가) 캡처되었습니다.`);
    });

    // 댓글 추가 처리
    addCommentBtn.addEventListener('click', () => {
      const text = commentText.value.trim();
      // 기본 캡처 시간이 0이면 현재 비디오 시간 사용
      const time = capturedTime || Math.floor(video.currentTime || 0);

      if(!text){
        showToast('댓글 내용을 입력하세요.');
        return;
      }

      const comment = {
        id: nextId++,
        time,
        text,
        author: '리뷰어(예시)',
        status: '대기중'
      };
      comments.push(comment);
      appendCommentToList(comment);
      appendCommentToTable(comment);
      commentText.value = '';
      // reset captured timestamp to avoid accidental reuse
      capturedTime = 0;
      timestampLabel.textContent = fmtTime(0);
      updateTableCount();
      showToast(`타임스탬프 댓글이 추가되었습니다. (${fmtTime(time)})`);
    });

    // 댓글 리스트에 항목 추가
    function appendCommentToList(c){
      const item = document.createElement('div');
      item.className = 'comment-item';
      item.dataset.id = c.id;

      item.innerHTML = `
        <div class="comment-left">
          <div class="time-badge" role="button" tabindex="0" data-time="${c.time}">${fmtTime(c.time)}</div>
          <div>
            <div class="comment-text">${escapeHtml(c.text)}</div>
            <div class="comment-meta">작성자: ${escapeHtml(c.author)} • 상태: <span data-state>${c.status}</span></div>
          </div>
        </div>
        <div style="display:flex;flex-direction:column;gap:8px;align-items:flex-end">
          <div style="display:flex;gap:6px">
            <button class="btn" data-action="goto">이동</button>
            <button class="btn" data-action="resolve">완료</button>
          </div>
        </div>
      `;

      // 이벤트: 타임배지 클릭 -> 해당 시간으로 이동
      const timeBadge = item.querySelector('.time-badge');
      timeBadge.addEventListener('click', () => { video.currentTime = c.time; video.play(); });

      // 이동 버튼
      item.querySelector('[data-action="goto"]').addEventListener('click', () => { video.currentTime = c.time; video.play(); });

      // 완료 버튼
      item.querySelector('[data-action="resolve"]').addEventListener('click', (ev) => {
        c.status = '완료';
        item.querySelector('[data-state]').textContent = '완료';
        // 동기화: 테이블에서도 상태 반영
        syncTableStatus(c.id, '완료');
        showToast(`댓글 #${c.id}이(가) 완료로 표시되었습니다.`);
      });

      // prepend (최신이 위)
      commentsList.prepend(item);
    }

    // 테이블 행 추가
    function appendCommentToTable(c){
      const tr = document.createElement('tr');
      tr.dataset.time = fmtTime(c.time);
      tr.dataset.id = c.id;
      tr.innerHTML = `
        <td><button class="timeLink time-badge">${fmtTime(c.time)}</button></td>
        <td>${escapeHtml(c.text)}</td>
        <td data-status>${c.status}</td>
        <td>${escapeHtml(c.author)}</td>
        <td class="table-actions">
          <button class="btn" data-action="goto">이동</button>
          <button class="btn" data-action="resolve">완료</button>
        </td>
      `;
      // goto 이벤트
      tr.querySelector('[data-action="goto"]').addEventListener('click', () => {
        video.currentTime = c.time;
        video.play();
      });
      // resolve 이벤트
      tr.querySelector('[data-action="resolve"]').addEventListener('click', function(){
        c.status = '완료';
        tr.querySelector('[data-status]').textContent = '완료';
        // 리스트 동기화
        syncListStatus(c.id,'완료');
        showToast(`테이블 항목이 완료 처리되었습니다.`);
        updateTableCount();
      });

      // timeLink 클릭시 이동
      const timeLinkBtn = tr.querySelector('.time-badge');
      timeLinkBtn.addEventListener('click', () => { video.currentTime = c.time; video.play(); });

      // prepend to table so newest at top
      feedbackTable.prepend(tr);
    }

    // 동기화 유틸: 리스트 -> 테이블 상태 변경
    function syncTableStatus(id, state){
      // table rows
      const tr = feedbackTable.querySelector(`tr[data-id="${id}"]`);
      if(tr){
        const statusCell = tr.querySelector('[data-status]');
        if(statusCell) statusCell.textContent = state;
      } else {
        // 테이블에 id 속성이 없을 수 있으므로 탐색 후 비교
        Array.from(feedbackTable.querySelectorAll('tr')).forEach(row => {
          if(row.dataset.id == id) {
            const statusCell = row.querySelector('[data-status]');
            if(statusCell) statusCell.textContent = state;
          }
        });
      }
      updateTableCount();
    }

    // 리스트 동기화
    function syncListStatus(id, state){
      const listItem = commentsList.querySelector(`.comment-item[data-id="${id}"]`);
      if(listItem){
        const stateEl = listItem.querySelector('[data-state]');
        if(stateEl) stateEl.textContent = state;
      }
    }

    // 승인/반려 버튼 동작
    approveBtn.addEventListener('click', () => {
      approvalStatus.textContent = '승인됨';
      approvalStatus.style.background = 'linear-gradient(90deg,var(--accent),var(--accent-2))';
      showToast('영상이 승인되었습니다. 회의에서 시연하세요.');
    });

    rejectBtn.addEventListener('click', () => {
      approvalStatus.textContent = '반려됨';
      approvalStatus.style.background = 'linear-gradient(90deg,var(--danger),#ff8a8a)';
      showToast('영상이 반려되었습니다. 운영팀에 피드백을 전송하세요.');
    });

    // 토스트 helper
    let toastTimer = null;
    function showToast(msg, timeout=2400){
      toast.style.display = 'block';
      toast.textContent = msg;
      if(toastTimer) clearTimeout(toastTimer);
      toastTimer = setTimeout(()=>{ toast.style.display = 'none'; }, timeout);
    }

    // 테이블에 이미 있는 예시 항목들에 동작 바인딩 (초기)
    document.querySelectorAll('#feedbackTable .timeLink').forEach(btn => {
      btn.addEventListener('click', () => {
        const time = btn.textContent.trim();
        locateTime(time);
      });
    });
    // 예시 완료 버튼 동작
    document.querySelectorAll('#feedbackTable .table-actions .btn').forEach(b => {
      // 이미 각 onclick에 inline 처리가 되어 있지만 추가 안전 바인딩
      // (일부 btns are '완료' which will call markResolved via inline)
    });

    // 외부에서 참조 가능한 유틸(테이블의 inline onclick과 같은)
    window.locateTime = function(timeStr){
      // mm:ss -> 초
      const parts = timeStr.split(':').map(x=>parseInt(x,10)||0);
      const sec = (parts[0]||0)*60 + (parts[1]||0);
      video.currentTime = sec;
      video.play();
      showToast(`${fmtTime(sec)} 위치로 이동합니다.`);
    };

    window.markResolved = function(btn){
      // table의 행을 완료로 표시
      const tr = btn.closest('tr');
      if(!tr) return;
      const statusCell = tr.querySelector('td:nth-child(3)');
      if(statusCell) statusCell.textContent = '완료';
      // 리스트 동기화: 찾을 수 있으면 표시
      const id = tr.dataset.id;
      if(id) syncListStatus(id,'완료');
      updateTableCount();
      showToast('항목이 완료 처리되었습니다.');
    };

    // 필터링
    filterSelect.addEventListener('change', () => {
      const val = filterSelect.value;
      Array.from(feedbackTable.querySelectorAll('tr')).forEach(tr => {
        const status = (tr.querySelector('[data-status]') || {}).textContent || '대기중';
        if(val === 'all') tr.style.display = '';
        else if(val === 'pending') tr.style.display = (status === '완료' ? 'none' : '');
        else if(val === 'done') tr.style.display = (status === '완료' ? '' : 'none');
      });
      updateTableCount();
    });

    // 토글: 테이블 컴팩트 모드 (압축)
    toggleCompact.addEventListener('click', () => {
      compactMode = !compactMode;
      if(compactMode){
        feedbackTable.style.fontSize = '12px';
        feedbackTable.querySelectorAll('td, th').forEach(el => el.style.padding = '6px 4px');
        toggleCompact.textContent = '압축 모드: ON';
      } else {
        feedbackTable.style.fontSize = '';
        feedbackTable.querySelectorAll('td, th').forEach(el => el.style.padding = '');
        toggleCompact.textContent = '테이블 압축 토글';
      }
    });

    // 테이블 항목 수 갱신
    function updateTableCount(){
      const visible = Array.from(feedbackTable.querySelectorAll('tr')).filter(tr => tr.style.display !== 'none');
      tableCount.textContent = visible.length;
    }
    updateTableCount();

    // 안전: HTML 이스케이프 (XSS 방지, 프로토타입이지만 안전모드)
    function escapeHtml(str){
      return String(str)
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#039;');
    }

    // 초기 안내 토스트
    showToast('프로토타입 로드 완료 — 캡처 버튼으로 타임스탬프를 찍고 댓글을 추가하세요.', 3800);

    // 접근성: 키보드로 타임배지 포커스 후 Enter로 이동
    document.addEventListener('keydown', (e) => {
      if(e.key === 'Enter' && document.activeElement && document.activeElement.classList.contains('time-badge')){
        const t = document.activeElement.dataset.time;
        if(t) locateTime(t);
      }
    });

  </script>
</body>
</html>
```

