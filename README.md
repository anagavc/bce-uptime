# bce-uptime

External uptime check for the Bring Cargo Express API. A GitHub Actions job probes the
public health endpoint every five minutes from outside the hosting provider. When the
API stops answering, the operations address gets an email; when it answers again, a
second email reports how long it was down. While it stays down, a reminder goes out
once an hour. `state.json` holds the last known state.

The repository is public only because GitHub runs scheduled workflows for free on
public repositories. It contains no credentials: the email provider key and the
addresses are repository secrets.
