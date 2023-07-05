package config

import (
	"flag"
	"os"
    "strconv"

    log "github.com/ml444/glog"
)

const (
	EnvKeyDebug        = "SERVICE_DEBUG"
	EnvKeyServiceDbDSN = "SERVICE_DB_DSN"
)

// Config contains the fields for running a server
type Config struct {
	Debug       bool
	EnableHTTP  bool
	EnableGRPC  bool
	HTTPAddr    string
	PprofAddr   string
	GRPCAddr    string

	DbDSN       string
}

var DefaultConfig Config

func init() {
	// NOTE: Flags have priority over Env vars.
	flag.BoolVar(&DefaultConfig.Debug, "debug", false, "enable APIs for pprof")
	flag.BoolVar(&DefaultConfig.EnableHTTP, "enable_http", true, "enable APIs for http")
	flag.BoolVar(&DefaultConfig.EnableGRPC, "enable_grpc", true, "enable APIs for grpc")
	flag.StringVar(&DefaultConfig.PprofAddr, "pprof_addr", ":5060", "Debug and metrics listen address")
	flag.StringVar(&DefaultConfig.HTTPAddr, "http_addr", ":5050", "HTTP listen address")
	flag.StringVar(&DefaultConfig.GRPCAddr, "grpc_addr", ":5040", "gRPC (HTTP) listen address")

	// Use environment variables, if set.
	if enable := os.Getenv(EnvKeyDebug); enable != "" {
		debug, err := strconv.ParseBool(enable)
		if err != nil {
			log.Errorf("err: %v", err)
		} else {
			DefaultConfig.Debug = debug
		}
	}
	if enable := os.Getenv("ENABLE_HTTP"); enable != "" {
		e, err := strconv.ParseBool(enable)
		if err != nil {
			log.Errorf("err: %v", err)
		} else {
			DefaultConfig.EnableHTTP = e
		}
	}
	if enable := os.Getenv("ENABLE_GRPC"); enable != "" {
		e, err := strconv.ParseBool(enable)
		if err != nil {
			log.Errorf("err: %v", err)
		} else {
			DefaultConfig.EnableGRPC = e
		}
	}
	if addr := os.Getenv("PPROF_ADDR"); addr != "" {
		DefaultConfig.PprofAddr = addr
	}
	if addr := os.Getenv("HTTP_ADDR"); addr != "" {
		DefaultConfig.HTTPAddr = addr
	}
	if addr := os.Getenv("GRPC_ADDR"); addr != "" {
		DefaultConfig.GRPCAddr = addr
	}
	if DefaultConfig.DbDSN == "" {
        DefaultConfig.DbDSN = os.Getenv(EnvKeyServiceDbDSN)
        if DefaultConfig.Debug {
            log.Info("DB:", DefaultConfig.DbDSN)
        }
    }
}

func GetConfig() *Config {
	return &DefaultConfig
}

