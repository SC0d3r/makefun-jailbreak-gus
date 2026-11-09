# makefun-jailbreak-gus

Entry for make.fun's `jailbreak-the-vault-01`: a scripted agent that talks a
guarded character into revealing each level's six-character code.

The entrypoint is `main.ts` (Node 22, standard library only). It reads the
env's origin from `MAKEFUN_ENV_URL`, chats through `POST /chat`, parses the
code from the reply, and submits it through `POST /guess`.
