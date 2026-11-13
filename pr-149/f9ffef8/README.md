PR #149 head f9ffef8 UI evidence. Real Go server (httpapi.New + engine.New, repo.OpenTest in-memory DB) serving the freshly built chatbot bundle on 127.0.0.1; local-login as fictitious user demo-owner.
Fictitious data only: project "Demo App", repo https://git.example/demo/app.git, workspace run ws-demo-1. Progress events appended via engine.RecordWorkspaceOpening (same path runner progress takes). No runner, Docker, or model calls.
- light-01-running: clone 12%, elapsed + "本阶段限时 10分钟"
- light-02-running-progress: clone 67%; output line "Authorization: token <fake>" is shown as "Authorization: [redacted]" (f9ffef8 fix)
- light-03-failed: failed state + retained-workspace note + retry button
- light-04-after-retry-composer: retry fills composer with "重试打开当前工作区 ws-demo-1，…"
- dark-05-failed / narrow390-06-failed: dark theme and 390px viewport
- light-07-ready: ready without Dockerfile warning -> card hidden
- interaction-running-progress-failed-retry.webm (17s, 1440x900)
