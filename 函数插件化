package main

import "fmt"

type type1 struct{}
type type2 struct{}

type Pluginfunc interface {
	Run()
}

var (
	funcMap = map[string]Pluginfunc{
		"type1": &type1{},
		"type2": &type2{},
	}
)

func (t *type1) Run() {
	fmt.Println("type1")
}

func (t *type2) Run() {
	fmt.Println("type2")
}
func main() {
	var funcs = []string{"type1", "type2"}
	for _, fname := range funcs {
		if f, ok := funcMap[fname]; ok {
			f.Run()
		}
	}
}
