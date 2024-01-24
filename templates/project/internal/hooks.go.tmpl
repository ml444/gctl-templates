package internal

import (
	"fmt"
	"os"
	"os/signal"
	"syscall"
)

func InterruptHandler(errCh chan<- error) {
	c := make(chan os.Signal, 1)
	signal.Notify(c, syscall.SIGINT, syscall.SIGTERM)
	terminateError := fmt.Errorf("%s", <-c)

	// Place whatever shutdown handling you want here

	errCh <- terminateError
}
