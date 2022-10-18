<script>

import * as Sentry from "@sentry/browser";
import { BrowserTracing } from "@sentry/tracing";

export default {
    mounted() {
      Sentry.init({
        dsn: "https://dba22ae42f05408c9bb8013aab1390d4@o1408302.ingest.sentry.io/6776949",
        release: "evalio@1.0.0",
        integrations: [new BrowserTracing()],
        tracesSampleRate: 0.01
      });
      console.log('Sentry is initialised');
  }
}

</script>