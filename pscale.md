https://davidparks.dev/blog/planetscale-deployment-with-prisma/

pscale branch create onboarding-demo initial-setup
pscale branch create onboarding-demo shadow

pscale connect onboarding-demo initial-setup --port 3309
pscale connect onboarding-demo add-reminders-table --port 3310




mysql://root@127.0.0.1:3309/onboarding-demo


pscale deploy-request create onboarding-demo  initial-setup

pscale connect onboarding-demo main --port 3309


shadowDatabaseUrl = env("SHADOW_DATABASE_URL")
