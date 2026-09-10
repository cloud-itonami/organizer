(ns organizer.test-runner
  (:require [clojure.test :as test]
            [organizer.methods.agent-test]
            [organizer.murakumo-test]))
(defn -main [& _]
  (let [r (test/run-tests 'organizer.methods.agent-test 'organizer.murakumo-test)]
    (when-not (zero? (+ (:fail r) (:error r))) (throw (ex-info "organizer tests failed" r)))))
